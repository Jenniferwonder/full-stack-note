---
Title: JSX (Lists)
Type: D
tags:
  - React
DateStarted: 2023-12-06
DateModified: 2024-01-17
DateDo: 
DateDone: 
DateDue: 
status: 
mindmap-plugin: basic
---

# JSX (Lists)

## Reference

### https://react.dev/learn#writing-markup-with-jsx

## component also can’t return multiple JSX tags

### You have to wrap them into a shared parent, like a `<div>...</div>` or an empty `<>...</>` wrapper

## Display Data

### JSX lets you put markup into JavaScript

### Curly braces let you “escape back” into JS so that you can embed some variable from your code and display it to the user
- You can add any JavaScript expression (something that evaluates to a single value) inside *curly braces*.
- An *object property* with dot notation
    - `<h1>{user.name}</h1>`
- A *template literal*
    - `return <h1>{`Cool ${title}`}</h1>;`
- The *returned value of a function*
    - `return <h1>{createTitle(title)}</h1>;`
- *ternary operators*
    - `return <h1>{title ? title : 'Default Title'}</h1>;`

## Conditional Rendering

### Case-1-`if...else`

### Case-2-`test? a:b`

### Case-3-`&&`

### 📌*[[Conditional]]*

## Render Lists

### `.map()` method

### `.filter()`
- 📌[[FilterList]]
- 📌[[ProductTableApp]]

### `key`
- `<li>` has a `key` attribute. For each item in a list, you should pass a string or a number that uniquely identifies that item among its siblings.

### 📌*[[Lists]]*