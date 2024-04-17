---
title: Deploying
tags:
  - TechSkills
DateStarted: 2022-11-29
DateModified: 2023-12-06
status:
---

## Questions

- How to deploy a React, Next.js+ Sanity project?
  - Vercel
- 自动化部署 (部署效率) ...
- [SEO](SEO)
- [CDN](CDN)
- [DNS](DNS)
- [Security](Security)
- [Server](Server)
- Monitor user traffic
- 图床

## Reference
- [大公司里怎样开发和部署前端代码？](https://link.juejin.cn?target=https%3A%2F%2Fwww.zhihu.com%2Fquestion%2F20790576 "https://www.zhihu.com/question/20790576")
- [前端高级进阶：前端部署的发展历程](https://juejin.cn/post/6844904086823780366 "https://juejin.cn/post/6844904086823780366")
- [如何部署网站？来比比谁的方法多 - 哔哩哔哩](https://www.bilibili.com/read/cv16179200)
- 你们公司项目发布流程是什么样的
- 前端资源发布路径怎么实现非覆盖式发布（平滑升级）？
    - [前端开发体系建设日记](https://link.segmentfault.com/?enc=ZpvInopx32IGK%2FvnIg2vLg%3D%3D.PJEv7fHpFxUMZ%2BIQuGQukLViiVDVM%2FejJlUOTokPCeZYXahz9lQzKfyK%2F2smXshy)
- SSR项目是如何发布的
### 原始部署

#### 1. 前端：

需要 web 服务器：**nginx**, apache, tomcat

#### 2. 后端

Java, Maven

### 宝塔 Linux 部署

### 前端托管
前端腾讯云 web 应用托管
- 小缺点：需要将代码放到代码托管平台
- 优势：不用写命令、代码更新时自动构建

### Docker 部署
可以将项目环境和项目代码一起打包成镜像，所有同学都能下载镜像，更容易分发移植

## 绑定域名

[DNS](DNS)

## 跨域问题解决

## [CI-CD](CI-CD.md)

- GitHub Actions (Auto Deploy)
- CI- Continuous Integration
- CD- Continuous Development

## Fullstack Deployment

Server-side apps need a server to execute your code

### PaaS

- Platform as a service
- Everything is set up for you without need to set up a server (Install **Nginx** and firewalls...)
- Only need to push your code to GitHub and select the repo from within the platform much like you do with Netlify

#### Render.com

With free tier

#### Heroku

Stop free tier since 2022

### Cloud Hosting

#### Google App Engine

##### 1.1. What and why?

- (Fully managed serverless application platform) - an easy and free way,
- It has a standard environment for Node.js
- Provide with a **Server** in the cloud that **scales automatically** based on the incoming traffic to your app

##### 1.2. How to use?

- It's easy to set up but you first need to have a <u>Google cloud platform account</u> and <u>Google command line tools</u> installed.
- Once done, you can go into your source code and create an `app.yaml` file, which is used to configure your cloud server. The only thing we need at this time is to specify a runtime of Node.js version `runtime: nodejs12`
- App engine will run your code by looking in the `package.json` file for a start script `"scripts": {"start": "node ."}`.
- From there, we can open the command line and run `gcloud app deploy`, that'll take a minute and then it will give you a URL where you can access your app publicly on the web.

- Unmanaged cloud hosting
- You rent out a Linux box and you can install whatever you want on it any Linux disk draw, any programs you want, set up Nginx and web servers and all that, but that's much more difficult

#### Lenode

- You can install the OS,
- Have to set everything up from scratch; you'll be installing your web servers, node.js or whatever your backend is using

#### AWS/ Azure

- Great for large projects with a lot of traffic
- Tons of services
