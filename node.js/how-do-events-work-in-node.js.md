---
Title: How do Events work in Node.js
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

## How do Events work in Node.js?

- an asynchronous event-driven JS runtime.
- Event loop - non-blocking
- ![](z-Assets/Pasted%20image%2020230301094039.png)

### How do Event and Callback work in Node?

- Built-in Event
  - ![](z-Assets/Pasted%20image%2020230301094450.png)
- Built own event: import `{EventEmitter}` from `events` module built in Node, then create a custom `eventEmitter` by instantiating the class, and register a callback that fires on the `lunch` event, then we can call `eventEmitter.emit('lunch')` which triggers callback function to run. - ![](z-Assets/Pasted%20image%2020230301095205.png)  
  This event-driven programming is useful when you have something that is CPU intensive.
