---
layout: post
title: Multiprocessing
category: work
tags: 
    - multiprocessing
    - data science
    - software engineering

---

i/o bound - reading and writing to disk (e.g. reading/writing files)
cpu bound - computation intensive

Multiprocessing (for cpu bound tasks)
multithreading (for i/o bound tasks)

Each process can have multiple threads

Variables/Dataspaces/Memory are shared between threads, but not processes

No two threads in python can occur simultaneously
- Intense CPU tasks are limited
time.perfcounter() used for multithreading
time.time() used for multiprocessing