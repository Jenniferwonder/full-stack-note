---
Title: Sanity
tags: TechSkills
DateStarted: 2023-01-09 
DateModified: 2023-02-07
status:
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 270
---

## 参考资料

- Sanity 版本更新情況[Sanity Studio v2 is deprecated – Sanity](https://www.sanity.io/help/studio-v2-vs-v3)
- 安裝步驟：[Getting DateStarted with Sanity](https://www.sanity.io/docs/getting-DateStarted-with-sanity)
- 官方文档[Sanity Studio](https://www.sanity.io/docs/sanity-studio)
- 管理后台[https://www.sanity.io/manage](https://www.sanity.io/manage)

## Plugins

[Code Input | Sanity.io plugin](https://www.sanity.io/plugins/code-input)

## How to set up a Sanity CMS?

- Set up a Sanity project in your project folder
- ❗Make sure to use the latest version of Sanity-v3 [Create a Sanity project](https://www.sanity.io/docs/create-a-sanity-project)
  - **Sanity account** – you need it to access your projects.
  - **Sanity project** – a place for your content represented as documents, stored by Sanity in the cloud. A single Sanity account can have an unlimited number of Sanity projects.
  - **Sanity Studio** – a React app to edit and publish content. Connected to a Sanity project via APIs. For now, it is installed on your computer. In the next steps, we'll cover how to deploy it to the web and share it with others.
- Understand the project folder structure
  - Medium-Clone Project
  - Portfolio-reference project

## Environment Variables/ Hiding Secrets

Config `.env.local` when using Sanity-v3 with Vite?

- create `.env.local` in ./client root folder
- in `tsconfig.json`, add `"types": "vite/client"`
- in `sanity.config.ts`, add value `import.meta.env.SANITY_STUDIO_PROJECT_ID`
  - See reference [Environment Variables](https://www.sanity.io/docs/environment-variables)
- Bug fix: [Property 'env' does not exist on type 'ImportMeta' in 3.0.0 · Issue #9539 · vitejs/vite · GitHub](https://github.com/vitejs/vite/issues/9539)
- [x] How to hide token/secrets in [[Sanity]] - Prevent environment variables bugs?

## Schema and Groq

- [x] How to create and design **Schemas** in Sanity?
- [x] How to CRUD Sanity data through Front-end operations?
  - [[Fetch API]]
  - [[Axios]]
  - Use `groq`
