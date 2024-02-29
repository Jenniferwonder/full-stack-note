---
Type: 
DateDo: 
DateDone: 
DateDue: 
Title: Testing
tags:
  - TechSkills
DateStarted: 2023-03-01
DateModified: 2024-01-03
status: 
mindmap-plugin: basic
---

# Testing

## Reference

### [如何使用 React Testing Library 和 Jest 测试 React 应用 · Issue #16 · vortesnail/blog · GitHub](https://github.com/vortesnail/blog/issues/16)

### [Test-Driven Development // Fun TDD Introduction with JavaScript - YouTube](https://www.youtube.com/watch?v=Jv2uxzhPFl4)

## Intro

### ![[Pasted image 20230308094955.png]]

### Best Practices
- Avoid including implementation details.
- Final users will have no notion of React. Rather than dealing with instances of rendered React components, your tests should wok with actual DOM nodes.
- Resemble software usage
- Maintainability in the long run - as long as you're not changing functionality any changes in the implementation of the component won't break your tests and slow you and your team down

### Why Testing?
- Discover defects or bugs before delivery to the client
- Guarantee the quality of the software you develop further by catching bugs before they find their way into a live application
- Reduce user complaints and save time and money

## TDD-Test Drivern Development Philosophy

### Unit Test
- Unit Test 单元测试 （代码帮你测试代码）

### Integration Test

### End-To-End Test

## React Testing Library

### Reference
- [React Testing Library | Testing Library (testing-library.com)](https://testing-library.com/docs/react-testing-library/intro/)
- Tutorials
    - [React Testing Library Tutorial (robinwieruch.de)](https://www.robinwieruch.de/react-testing-library/)

## Jest

### Reference
- [Getting Started · Jest](https://jestjs.io/docs/getting-started)
- Tutorials
    - [React Testing Tutorial (Jest + React Testing Library) (youtube.com)](https://www.youtube.com/watch?v=ML5egqL3YFE)

### Two tools React endorses to structure your tests.

### Good iteration speed

### Powerful features, like *mocking* modules so you can have more control over how the code executes, to make sure your unit testing is standalone.

### A JS test runner that lets you access an artificial DOM called jsdom. While jsdom is an approximation of how the browser works, it's often good enough for testing React component.

## 📌[[Cypress]]

## 📌[[Storybook]]

## Mocha

## Joint Debugging 联调 (多人协作效率)

## Monitor 监控报警 （线上问题提前预知）