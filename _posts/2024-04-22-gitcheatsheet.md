---
layout: post
title: Git cheatsheet - start quickly for complete beginners.
category: work
tags: 
    - git
    - software engineering
    - beginners
---
Are you starting out on your version control system journey and want to get started quickly? Using the File Explorer as the remote repository? Then read on!

I decided to write my own as I found that some cheatsheets do not have all the commands I needed, to get the ball rolling when I first started out.
In this sheet, you will also find the commands for setting up a git remote repo on the file repository. The commands are mostly the same,
but I sectioned out the commands for this special case [here](#using-file-explorer-as-remote-repository).


You will need to [install git](https://git-scm.com/downloads) to get started.


## Setting up

| Command                                                    | Description                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| <em>git config \-\-global user-name 'myname'</em>          | Setup name. Name will appear in branches when you start doing commits |
| <em>git config \-\-global user.email 'me@example.com'</em> | Setup email                                                           |
| <em>git config \-\-list</em>                               | Check your setup in the config file. Press q to exit                  |

More ways to customize you setup [here](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).


##### Using File Explorer as remote repository

If you are not using GitHub or other server-based tools to store your remote repository, 
here is how you set up an empty repo on File Explorer on Windows, like a drive in the network.
This is an alternative to 'Creating a new repository' in Github to do things completely locally.

| Command                                     | Description                                  |         
|---------------------------------------------|----------------------------------------------|
| <em>cd  \\\\my-remote-folder\my_repo</em>   | Navigate to the remote folder on the network |
| <em>git init \-\-bare</em>                  | Initialise remote repository there           | 


## Working locally

| Command                                                  | Description                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <em>git init</em>                                        | Initialise a git repository                                                                                                           |
| <em>git add  filename.py</em>                            | Brings file to staging area which stores info to next commit                                                                          |
| <em>git add .</em>                                       | Add all files in current folder to staging                                                                                            |
| <em>git status<em>                                       | Check which files are in the staging area                                                                                             |
| <em>git commit -m "Type your message"</em>               | Commit                                                                                                                                |
| <em>mkdir .gitignore</em>                                | Create <em>.gitignore</em> <br> List file names in this file and commit <em>.gitignore</em> to see the ignore effects come into play. |
| <em>git branch</em>                                      | See which branch you are in                                                                                                           | 
| <em>git checkout -b</em>                                 | Create a new branch based on the current branch                                                                                       |
| <em>git checkout -b new_branch_name old_branch_name</em> | Create a new branch based on an old                                                                                                   |
| <em>git checkout  other_branch</em>                      | Go to the other branch                                                                                                                |
| <em>git branch</em>                                      | Show all branches                                                                                                                     | 
| git merge other_branch                                   | Merge other branch into current branch                                                                                                |
| <em>git log --oneline</em>                               | Show all commits made in a branch                                                                                                     |


## Working remotely

| Command                                                                       | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <em>git clone \\\\my-remote-folder\\my-repo</em>                              | Clone a remote repo                                                                                                                                                          |                                                                                                                   |
| <em>git remote add origin \\\\my-remote-folder\\my-repo</em>                  | Set up the remote repository in your local repo. <br><em>origin</em> as the nickname of the remote repo you call in your local repo. <br> File path can also be a hyperlink. |
| <em>git push -u origin main<em>                                               | Push the current branch to the remote repo, origin with branch name main                                                                                                     |
| <em>git remote -v</em>                                                        | View all remote connections                                                                                                                                                  |
| <em>git branch -r -v</em>                                                     | View last commit in all branches                                                                                                                                             |
| <em>git push origin -delete main</em>                                         | Delete the remote branch main                                                                                                                                                |



