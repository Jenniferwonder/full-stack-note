---
title: File System
type: D
tags:
  - NodeJS
DateStarted: 2024-01-26
DateModified: 2024-04-17
status: 
---

## File System

Built-in file system module called `fs`, which can read, write and delete files on the file system among other things, and it can also do things in a blocking or non-blocking way.

### Eg. Read File

Import two functions from the file system module, called `{readFile, readFileSync}`. Anytime you see a function ends in `sync` think blocking.  
We can read a text file in Node by simply passing the path to that file and we'll specify the encoding as `'utf8'`.

#### Blocking

- ![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Pasted-image-20230301100205.png)

#### Non-Blocking

- Tip1: Use Callback
  - ![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Pasted-image-20230301100308.png)
- Tip 2: Use Promise-based solutions
  - Import `readFile` from the `promises` namespace, which gives us a function returning a promise when called
  - ![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Pasted-image-20230301100827.png)
  - ![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Pasted-image-20230301100907.png)
