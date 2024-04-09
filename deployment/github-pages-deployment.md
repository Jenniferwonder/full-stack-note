---
DateStarted: 2023-11-30
DateModified: 2023-12-06
---
# GitHub Pages
## Purpose
- [x] 免费部署前端项目至 `.github.io` 域名对应仓库名 ✅ 2024-04-01

## How
`.github/workflows/deploy.yml`
GitHub Repository > Setting > Pages > Source (Branch, Folder)

## gh-pages 用法
### 部署同一仓库多个文件夹
[GitHub Pages for a repo with multiple subfolders · community · Discussion #58276 · GitHub](https://github.com/orgs/community/discussions/58276)
[Deploy a sub-folder to Github Pages | by Akshay Kumar Nalatawad | Medium](https://medium.com/@akshaykumarnalatawad/deploy-a-sub-folder-to-github-pages-9151a362e139)
### 部署项目 `main` 分支中指定文件夹代码至 `gh-pages` 分支 (指定文件夹) （gh-pages）
❓适合框架类项目，如 Astro 吗
#### Related Project
- 📌[build: update key in deploy.yml · Jenniferwonder/js-note@8627822 · GitHub](https://github.com/Jenniferwonder/js-note/actions/runs/8494743313/workflow)
#### Reference
> ⭐[GitHub - peaceiris/actions-gh-pages: GitHub Actions for GitHub Pages 🚀 Deploy static files and publish your site easily. Static-Site-Generators-friendly.](https://github.com/peaceiris/actions-gh-pages?tab=readme-ov-file#%EF%B8%8F-create-ssh-deploy-key)
^87wvdr
- [How to deploy a website with GitHub pages from a folder other than "docs/"? - Stack Overflow](https://stackoverflow.com/questions/77726552/how-to-deploy-a-website-with-github-pages-from-a-folder-other-than-docs#:~:text=You%20can%20use%20the%20peaceiris%2Factions-gh-pages%20github%20action%20to,will%20then%20deploy%20the%20contents%20of%20this%20branch.)
- [如何用Github的gh-pages分支展示自己的项目 - 牧云云 - 博客园](https://www.cnblogs.com/MuYunyun/p/6082359.html)
- `git subtree push --prefix=dist origin gh-pages`

#### 🐛 Bugs
>[Action failed with "The process '/usr/bin/git' failed with exit code 128" - Stack Overflow](https://stackoverflow.com/questions/76023778/action-failed-with-the-process-usr-bin-git-failed-with-exit-code-128)

🐛 `Action failed with "The process '/usr/bin/git' failed with exit code 128"`
- [build: update deploy.yml · Jenniferwonder/js-note@95a98e6 · GitHub](https://github.com/Jenniferwonder/js-note/actions/runs/8494431951)
🐛`Action failed with "The process '/usr/bin/ssh-add' failed with exit code 1"`

##### ✅ Resolve
- Refer to: [[GitHub Pages Deployment#^87wvdr|actions-gh-pages]]
	- Correctly create ssh key, and add the `.pub` one to the repo's `GitHub Action Deploy Key` page with the name `ACTIONS_DEPLOY_KEY`, and the other one with the same name to the repo's `Secrets`
	- Change `secrets.GitHub_Token` to `secrets.Actions_DEPLOY_KEY`
- ![[z-github-action-deploy-key.png|400]]
### Deploy Key and Secrets in GitHub Action 
- [Deploy key | Code Cookbook](https://michaelcurrin.github.io/code-cookbook/recipes/ci-cd/github-actions/tokens/deploy-key.html#:~:text=Go%20to%20repo%20Settings.%20Go%20to%20Deploy%20Keys.,machine%20can%20deploy%29.%20Optionally%20tick%20Allow%20write%20access.)
- [How to Use GitHub Deploy Keys](https://dylancastillo.co/how-to-use-github-deploy-keys/)
- [Automatic token authentication - GitHub Docs](https://docs.github.com/en/actions/security-guides/automatic-token-authentication)
- [Using secrets in GitHub Actions - GitHub Docs](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)
- [Managing deploy keys - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/managing-deploy-keys#deploy-keys)
### Traffic Badge
- [Traffic to Badge · Actions · GitHub Marketplace · GitHub](https://github.com/marketplace/actions/traffic-to-badge)
- [GitHub - MuYunyun/blog at traffic](https://github.com/MuYunyun/blog/tree/traffic?tab=readme-ov-file)
### Astro Project Workflow Template
#### Related Project
- 🚀[GitHub - Jenniferwonder/js-note: JS Notes (built with Astro-Starlight, and hosted on GitHub Pages, with Chinese-English Support)](https://github.com/Jenniferwonder/js-note)
	- [fix: hero links error · Jenniferwonder/js-note@2991b5d · GitHub](https://github.com/Jenniferwonder/js-note/actions/runs/8491485915/workflow)
#### Reference
- ⭐[Deploy your Astro Site to GitHub Pages | Docs](https://docs.astro.build/en/guides/deploy/github/)
- [How to deploy an Astro site to GitHub Pages - DEV Community](https://dev.to/github/how-to-deploy-a-static-site-in-any-framework-of-your-choice-github-pages-neh)

### Vite + React Project Workflow Template
#### Related Project
- 🚀[GitHub - Jenniferwonder/learn-react: ⚡React code demos & notes (React 代码示例与学习笔记)](https://github.com/Jenniferwonder/learn-react)
#### Reference
- Vite Deployment Config

- *托管个人网站和博客：* 用户可以使用 GitHub Pages 托管个人网站、博客或简历等静态页面。通过将静态文件（HTML、CSS、JavaScript 等）推送到 GitHub 仓库中，GitHub Pages 会自动构建并将这些文件发布为可通过浏览器访问的网站。
- *托管项目文档：* GitHub Pages 是一个理想的地方，用于托管项目的文档。通过将项目文档以 Markdown 格式编写并与 GitHub 仓库一起存储，可以轻松地创建漂亮的文档网站，方便团队和用户阅读。
- *展示开源项目：* 开发者可以使用 GitHub Pages 创建用于展示开源项目的静态页面。这可以包括项目的主页、示例演示、使用说明等，以提供更好的项目展示和交流。
- *在线简历和个人作品集：* GitHub Pages 提供了一个简单而免费的方式，让开发者创建在线简历、个人作品集或在线展示技能和项目的页面。
- *支持自定义域名：* GitHub Pages 支持自定义域名，用户可以将自己拥有的域名与 GitHub Pages 链接，使其网站能够通过自定义域名访问。
- *免费：* GitHub Pages 是免费的，并且它提供了很多方便的功能，使用户能够轻松地托管和管理静态网站，而无需付费。
- 访问问题
    - GitHub 域名被墙： GitHub 的主域名 `github.com` 曾经在中国大陆被墙，导致访问速度慢。但 GitHub 提供了使用 `githubusercontent.com` 作为 CDN 域名来提供 GitHub Pages 服务，该域名通常较少受到限制。
    - 使用自定义域名： 如果你使用了自定义域名，例如 `yourdomain.com`，在中国大陆仍然可能会受到访问限制。为了提高访问速度，你可以考虑使用国内 CDN 服务，将静态资源加速到国内节点。
    - 加速和备用方案： 有一些服务提供商和工具可以帮助在中国大陆提高 GitHub Pages 的访问速度。例如，使用 CDN 服务、云服务提供商，或者将静态文件部署到国内服务器，以备用方案。

### Gitee Pages







