---
title: 组件间通信-react-props
topic:
  - Component-Basics
type: D
tags:
  - React
DateStarted: 2024-04-12
DateModified: 2024-04-17
Datereviewed: 2024-04-12
reviewed: 1
difficulty: 
status: 
comment: 
---

# 组件间通信-react-props-state-context

#### [React 组件间的通信有哪些？](https://github.com/haizlin/fe-interview/issues/648)

#### ❓[React 非兄弟组件如何通信？](https://github.com/haizlin/fe-interview/issues/652)

#### [React 兄弟组件如何通信？](https://github.com/haizlin/fe-interview/issues/651)

#### [React 非父子组件如何通信？](https://github.com/haizlin/fe-interview/issues/650)

#### [React 父子组件如何通信？](https://github.com/haizlin/fe-interview/issues/649)

### React Key

#### [需要把 keys 设置为全局唯一吗？](https://github.com/haizlin/fe-interview/issues/884)

#### [React 中遍历时为什么不用索引作为唯一的 key 值？](https://github.com/haizlin/fe-interview/issues/643)

#### [React 中的 key 有什么作用？](https://github.com/haizlin/fe-interview/issues/642)

#### React key 是干嘛用的 为什么要加？key 主要是解决哪一类问题的

### Props

#### [React 组件的 state 和 props 两者有什么区别？](https://github.com/haizlin/fe-interview/issues/645)

#### [怎么在 JSX 里使用自定义属性？](https://github.com/haizlin/fe-interview/issues/813)

#### [怎么在 JSX 里属性可以被覆盖吗？覆盖的原则是什么？](https://github.com/haizlin/fe-interview/issues/814)

#### [如何给非控组件设置默认的值？](https://github.com/haizlin/fe-interview/issues/894)

#### [为什么说 React 中的 props 是只读的？](https://github.com/haizlin/fe-interview/issues/924)

#### [如果组件的属性没有传值，那么它的默认值是什么？](https://github.com/haizlin/fe-interview/issues/900)

#### [在 React 中组件的 props 改变时更新组件的有哪些方法？](https://github.com/haizlin/fe-interview/issues/824)

#### [React 中验证 props 的目的是什么？](https://github.com/haizlin/fe-interview/issues/790)

#### [React 中怎么检验 props？](https://github.com/haizlin/fe-interview/issues/787)

#### [React 中你有使用过 getDefaultProps 吗？它有什么作用？](https://github.com/haizlin/fe-interview/issues/789)

#### [给组件设置很多属性时不想一个个去设置有什么办法可以解决这问题呢？](https://github.com/haizlin/fe-interview/issues/784)

#### [immutable 的原理是什么？](https://github.com/haizlin/fe-interview/issues/823)

#### [你对 immutable 有了解吗？它有什么作用？](https://github.com/haizlin/fe-interview/issues/822)

#### [React 中你有使用过 propType 吗？它有什么作用？](https://github.com/haizlin/fe-interview/issues/788)

#### [使用 PropTypes 和 Flow 有什么区别？](https://github.com/haizlin/fe-interview/issues/869)

### Portal & Slot

#### [举例说明 React 的插槽有哪些运用场景？](https://github.com/haizlin/fe-interview/issues/934)

#### [你有用过 React 的插槽(Portals)吗？怎么用？](https://github.com/haizlin/fe-interview/issues/933)

#### [请说说 React 中 Portal 是什么？](https://github.com/haizlin/fe-interview/issues/687)

## React 组件间通信 (props, children)

- 概念
- ![z-React-CDD-组件插槽用法.png|400](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/z-React-CDD-%E7%BB%84%E4%BB%B6%E6%8F%92%E6%A7%BD%E7%94%A8%E6%B3%95.png)

- 组件的 `children` 子元素
- ![React-CDD-插槽-children.png|350](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/React-CDD-%E6%8F%92%E6%A7%BD-children.png)
  - ![React-CDD-children.png|425](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/React-CDD-children.png)
  - 弊端
    - children 数量被限制
      - 1 个 (值为对象)
        - `children: button`
      - 多个 (值为对象数组)
        - `children: [button, ...]`
  - 限制只能传一个元素
  - ![React-CDD-children-1.png](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/React-CDD-children-1.png)
- `props` 属性传递 React 元素
  - ![React-CDD-props.png|325](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/React-CDD-props.png)

![1701567850607.png|500](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/1701567850607.png)
