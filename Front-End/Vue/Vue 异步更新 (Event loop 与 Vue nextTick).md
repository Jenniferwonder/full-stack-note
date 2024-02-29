---
Title: Vue 异步更新 (Event loop 与 Vue nextTick)
Topic:
  - Async
Type: D
tags:
  - JavaScript
  - Vue
DateStarted: 2024-02-20
DateModified: 2024-02-20
DateDo: 
DateDone: 
DateDue: 
DateReviewed: 
Reviewed: 
Difficulty: 
status: 
Comment:
---
# Vue 异步更新 (Event loop 与 Vue nextTick)
### Reference
- [Vue 异步更新 - nextTick 为什么要 microtask 优先](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2Fqingzhou729%2Fstudy%2Fissues%2F15 "https://github.com/qingzhou729/study/issues/15")
- 🏷️[Event Loop-事件循环](Event%20Loop-事件循环)

#### vue nextTick 为什么要优先使用微任务实现？

1） Vue nextTick 的源码实现，优先级判断，总结就是 `Promise > MutationObserver > setImmediate > setTimeout`

2）这里优先使用 Promise，因为根据 event loop 与浏览器更新渲染时机，使用微任务，本次 event loop 轮询就可以获取到更新的 dom

3）如果使用宏任务，要到下一次 event loop 中，才能获取到更新的 dom