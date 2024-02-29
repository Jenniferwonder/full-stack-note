---
Title: GitHub 访问问题
Type: 
tags:
  - Git
DateStarted: 2024-01-08
DateModified: 2024-01-08
DateDo: 
DateDone: 
DateDue: 
status:
---
# GitHub 访问问题
## 问题描述
- `Access to script at 'https://github.githubassets.com/assets/app_assets_modules_react-code-view_pages_CodeView_tsx-28af03842713.js' from origin 'https://github.com' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource.`
## IP 地址查询
- [What Is My IP Address? Free IP Lookup](https://www.ipaddress.com/)
- GitHub 最新地址：
	- [hosts](https://raw.githubusercontent.com/521xueweihan/GitHub520/master/hosts)
## 命令行操作
### 修改 hosts 文件
- 管理员权限打开 hosts 文件，复制 GitHub 最新 IP 地址
	-  `C:\Windows\System32\drivers\etc\hosts`
- 关注 Hosts 自动更新工具：
	- [Releases · oldj/SwitchHosts](https://github.com/oldj/SwitchHosts/releases)
### 测试 DNS 域名数据请求情况
- `ping github.com`
### 刷新 DNS
- `ipconfig /flushdns`
## Reference
- [完美解决github访问速度慢、图片无法显示问题 - 简书](https://www.jianshu.com/p/58c4a3edb668)
- [🔨工具：解决Github挂图及龟速访问 | RealCat](https://vincentqin.tech/posts/manage-pc-hosts/#%E8%87%AA%E5%8A%A8%E6%96%B9%E5%BC%8F)
- [告别无法访问的github（附解决方案）-阿里云开发者社区](https://developer.aliyun.com/article/813040)