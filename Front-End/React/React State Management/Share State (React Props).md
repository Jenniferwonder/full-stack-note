---
Title: Share State (Props)
Type: D
tags:
  - React
  - React/State
DateDo: 
DateDone: 
DateDue: 
status: 
DateStarted: 2023-12-06
DateModified: 2023-12-06
mindmap-plugin: basic
---

# Share State (React Props)

## Reference

### [Sharing State Between Components • React](https://beta.reactjs.org/learn/sharing-state-between-components#recap)
- When you want to coordinate two components, move their state to their common parent.
- Then pass the information down through props from their common parent.
- Finally, pass the event handlers down so that the children can change the parent’s state.
- It’s useful to consider components as “controlled” (driven by props) or “uncontrolled” (driven by state).

## ⭐Props (proptypes, defaultprops, etc)

### Read-only information that's passed to components

## Component & App Level

### ![[Paste image 1701567850607image.png]]

### Move the *state* up from the component to its parent

## Pass the *state* and *Event Handlers* as *props* to each component used in the parent app

### `<MyButton count={count} onClick={handleClick} />`

## Let the child component read the *props*

### `MyButton(props)`
- the child component, can accept those props as its first function parameter
- If you `console.log()` props, you can see that it's an object with properties.

### `MyButton({ count, onClick })`
- use [object destructuring](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) to explicitly name the values of props inside your function parameters

## Case

### 📌[[ShareClickApp]]

### 📌[[FilterList]]

### 🚀MiniApp
- 📌[[Tic-Tac-Toe]]