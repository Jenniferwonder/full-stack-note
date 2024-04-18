---
title: Monorepo
topic:
  - Git
type: O
tags:
  - Git
DateStarted: 2024-02-23
DateModified: 2024-04-17
DateDue: 
ewed: 
reviewed: 
difficulty: 
status: 
comment: 
---

# Monorepo

## Reference

- [All in one：项目级 monorepo 策略最佳实践 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/348898271)

## 目录结构

- ```md
  .
   ├── lerna.json
   ├── package.json
   └── packages/ # 这里将存放所有子 repo 目录
       ├── project_1/
       │ ├── index.js
       │ ├── node_modules/
       │ └── package.json
       ├── project_2/
       │ ├── index.js
       │ ├── node_module/
       │ └── package.json
       ...
  ```

- 将不同项目的目录汇集到一个目录之下

## 优势

- 代码复用更容易
  - 很容易抽离出各个项目共用的业务组件或工具，并通过 TypeScript，Lerna 或其他工具进行代码内引用
- 依赖管理更简单
  - 由于项目之间的引用路径内化在同一个仓库之中，我们很容易追踪当某个项目的代码修改后，会影响到其他哪些项目。通过使用一些工具，我们将很容易地做到版本依赖管理和版本号自动升级
- 代码重构更便捷
  - 能够明确知道您的代码的影响范围，并且能够对被影响的项目可以进行统一的测试，这会鼓励您不断优化代码
- 倡导开放、透明、共享组织文化，利于开发者成长、代码质量提升
  - 每个开发者都被鼓励去查看，修改他人的代码（只要有必要），同时，也会激起开发者维护代码，和编写单元测试的责任心
  - 会形成一种良性的技术氛围，从而保障整个组织的代码质量

## 劣势

- 项目粒度的权限管理变得非常复杂
  - 可以将 monorepo 策略实践在「项目级」这个层次上
- 在 monorepo 策略下，新人可能不得不花更多精力来理清各个代码仓库之间的相互逻辑
- 对于公司级别的 monorepo 策略而言，需要专门的 VFS 系统，自动重构工具的支持
