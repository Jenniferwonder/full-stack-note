---
Title: Event Update
Type: D
tags:
  - React
  - React/State
DateStarted: 2023-12-06
DateModified: 2023-12-06
DateDo: 
DateDone: 
DateDue: 
status: 
mindmap-plugin: basic
---

# Event Update

## Reference

### [Reacting to Input with State • React](https://beta.reactjs.org/learn/reacting-to-input-with-state)
- *Identify* your component’s different visual states
- *Determine* what triggers those state changes (Human/ computer input)
- *Represent* the state in memory using `useState`
- *Remove* any non-essential state variables
- *Connect* the event handlers to set the state

## Respond to Events/ Inputs

### `onClick={handleClick}`
- 📌[[Click]]
- 📌[[UpdateClick]]
- 📌[[RemoveBg]]
- 📌[[Gallery]]
    - Store Boolean as state
    - Conditional rendering
    - `handleNextClick(){}`
    - `handleMoreClick(){}`

### `onSubmit` (Form Handling)
- 📌[[Quiz]]
    - `async function`
        - `try {await...} catch (err) {...}`
    - `new Promise((resolve, reject) =>{ })`
        - `setTimeout()`
        - `new Error()`
- 📌[[EditProfile]]

### `onChange` (input text & checkbox)
- `onChange={(e) => onFilterTextChange(e.target.value)}`
- `onChange={(e) => onInStockOnlyChange(e.target.checked)}`
- 🏷️Table
    - 📌[[ProductTableApp]]
    - 📌[[FilterList]]
- 📌[[MailSelect]]

### `onFocus` & `onPointerMove`
- 📌[[MailHighlight]] (Highlight & Star)

## Update Screen (Event Handlers)

### `useState` Hook
- `import { useState } from "react";`
- `import { React } from "react";`

### State as a snapshot
- Setting it does not change the state variable you already have, but instead triggers a re-render.
    - 📌[[Message]]
        - State as a snapshot

### Queueing a series of state updates
- replacing `setScore(score + 1)` with `setScore(s => s + 1)` fixes the “+3” button.
    - 📌[[Scores]]
        - Queueing state updates

### Update objects/ arrays in state
- use the `...` spread syntax to copy objects and arrays that you want to change.
    - 📌[[InfoChange]]
        - Update objects in state
- Use [Immer](https://github.com/immerjs/use-immer) instead of `useState` in this case to reduce repetitive code.
    - 📌[[ImmerInfoChange]]