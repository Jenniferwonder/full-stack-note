---
Title: About Node & Runtime
Type: D
tags:
  - NodeJS
DateStarted: 2024-01-26
DateModified: 2024-01-26
DateDo: 
DateDone: 
DateDue: 
status:
---
## About Node & Runtime
- A JS runtime to run JS in the server  
- ![[Pasted image 20230310115943.png]]
### Understand Runtime
- Unique identifiers
- `global` similar to `window` object, value of which can be accessed anywhere
- `process.platform` gives you access to the currently running node process, with which we can check the current platform or OS
- `process.env.USER` to grab an environment variable from your server