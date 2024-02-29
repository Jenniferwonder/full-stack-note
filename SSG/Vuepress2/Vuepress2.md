---
Title: Vuepress 2
Type: D
tags:
DateStarted: 2023-11-30
DateModified: 2023-12-01
DateDo:
DateDone:
DateDue:
status:
---

# Vuepress 2

## Related

- [数据库怎样存储 Markdown 文档数据](数据库怎样存储%20Markdown%20文档数据.md)

## Case

- 文档是基于 [VuePress2](https://v2.vuepress.vuejs.org/) 构建，图使用 [Fabric.js](http://fabricjs.com/) 绘制，通过 Github Actions 自动部署, 大家可以在右上角访问 Github 地址，或者访问每个页面下方的修改链接，随时通过 PR 的方式共建这个知识图谱， Java，Python 等岗位的知识图谱正在制作中，欢迎一起共建一个最好的计算机知识图谱
- 路线图的数据格式大家可以参考 [docs/index.md](https://github.com/shengxinjing/it-roadmap/blob/main/docs/index.md)
- 这个网站会一直以静态的形式存在，不需要登录，不需要关注公众号，源码和文稿全部在 Github，欢迎大家一起来提 PR 共建
- 文件夹 docs 下面就是全部的文档，roadmap 组件负责渲染路线图，动态渲染
- Interactive Mindmap
- Link to **Book Site** ([Books](https://books.halfrost.com/))
  - Edit this page
  - Last modified
  - Github Comment

## Intro

### 为什么不选其他方案

- Nuxt (Designed for building applications, while VuePress is more **lightweight** and focused on **content-centric static sites**.)
- Vitepress (More opinionated and less **configurable**. It does not support plugins.)
- Gitbook (Its **development reload performance** is intolerable with a large amount of files. The default **theme** also has a pretty limiting navigation structure, and the theming system is, again, not Vue based. The **team behind** GitBook is also more focused on turning it into a commercial product rather than an open-source tool.)
- Hexo (**Theming** system is static and string-based - we want to take advantage of Vue for both the **layout and the interactivity**. Also, Hexo's **Markdown rendering** isn't the most flexible to configure)
- Docsify / Docute (Both fully runtime-driven and therefore not **SEO**-friendly. If you don't care for SEO and don't want to mess with **installing dependencies**, these are still great choices.)

### 官方

- A VuePress site is in fact a single-page application (SPA) powered by [Vue](https://vuejs.org/) and [Vue Router](https://router.vuejs.org/).
  - Routes are generated according to the relative path of your markdown files. Each Markdown file is compiled into HTML with [markdown-it](https://github.com/markdown-it/markdown-it) and then processed as the template of a Vue component. This allows you to directly use Vue inside your Markdown files and is great when you need to embed dynamic content.
  - During development, we start a normal dev-server, and serve the VuePress site as a normal SPA. If you’ve used Vue before, you will notice the familiar development experience when you are writing and developing with VuePress.
  - During build, we create a server-rendered version of the VuePress site and render the corresponding HTML by virtually visiting each route. This approach is inspired by [Nuxt](https://nuxtjs.org/)'s `nuxt generate` command and other projects like [Gatsby](https://www.gatsbyjs.org/)

### 使用 Vuepress 2 不需要搭建数据库吗

- VuePress 2 是一个静态网站生成器，它生成的网站是基于静态文件的，而不需要后端服务器或数据库。这意味着对于简单的个人博客，你可以直接使用 Markdown 文件来编写博客内容，而不需要设置数据库。
- 在 VuePress 2 中，你的博客内容以及网站的结构是通过 Markdown 文件和特定的目录结构来定义的。当你运行 `npm run build` 时，VuePress 2 会将这些 Markdown 文件转换成静态的 HTML、CSS 和 JavaScript 文件，这些文件可以直接通过浏览器访问，而不需要动态生成内容或从数据库中检索数据。
- 对于不需要用户登录、评论或其他动态交互的静态博客，VuePress 2 提供了一种简单且高效的方式来构建和部署。
- 如果你的博客需要与数据库进行交互，比如用户评论、用户登录等功能，那么你可能需要考虑使用其他技术栈，例如前端框架（Vue.js、React、Angular）与后端框架（Node.js、Express、Django、Flask）以及数据库（MongoDB、MySQL、PostgreSQL）的组合。在这种情况下，你可能需要搭建一个后端服务器，并使用数据库来存储和检索数据。

## Use

### 用 Vuepress 2 怎样搭建个人博客

- ![](z-Assets/Vuepress%202.png)
- ![](z-Assets/Vuepress%202-1.png)
- ![](z-Assets/Vuepress%202-2.png)
- ![](z-Assets/Vuepress%202-3.png)
- ![](z-Assets/Vuepress%202-4.png)
