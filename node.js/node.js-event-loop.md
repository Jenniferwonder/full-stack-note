---
title: Node.js Event Loop
topic:
  - Async
type: D
tags:
  - JavaScript
  - NodeJS
DateStarted: 2024-02-20
DateModified: 2024-04-17
Datereviewed: 
reviewed: 
difficulty: 
status: 
comment: 
---

# Node.js Event Loop

### Reference

- [浏览器与 Node 的事件循环(Event Loop)有何区别?](https://link.juejin.cn?target=https%3A%2F%2Fzhuanlan.zhihu.com%2Fp%2F54882306 "https://zhuanlan.zhihu.com/p/54882306")
- [浏览器与 Node 的事件循环(Event Loop)有何区别?](https://link.juejin.cn?target=https%3A%2F%2Fzhuanlan.zhihu.com%2Fp%2F54882306 "https://zhuanlan.zhihu.com/p/54882306")
- [The Node.js Event Loop, Timers, and process.nextTick()](https://link.juejin.cn?target=https%3A%2F%2Fnodejs.org%2Fen%2Fdocs%2Fguides%2Fevent-loop-timers-and-nexttick%2F "https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/")

### Node 中的 process.nextTick

有很多文章把 Node 的 `process.nextTick` 和微任务混为一谈，但其实并不是同一个东西  
process.nextTick 是 Node.js 自身定义实现的一种机制，有自己的 `nextTickQueue`  
**process.nextTick 执行顺序早于微任务**  
**示例**

```javascript
console.log("start");
setTimeout(() => {
	console.log("timeout");
}, 0);
Promise.resolve().then(() => {
	console.log("promise");
});
process.nextTick(() => {
	console.log("nextTick");
	Promise.resolve().then(() => {
		console.log("promise1");
	});
});
console.log("end");
// 执行结果 start end nextTick  promise promise1 timeout
```
