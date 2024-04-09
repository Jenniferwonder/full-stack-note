---
Title: VS Code 安装包解析报错解决思路与方法
tags:
  - TechSkills
status: ""
DateStarted: 2022-11-11
aliases: 
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 272
DateModified: 2023-12-01
---

VS Code 安装包解析报错解决思路与方法
创作时间：2022 年 11 月 11 日

### 前言

代码报错，遇到 BUG，是很好锻炼解决问题能力的机会，比如当 VS Code 中出现 @babel/preset-env 安装包解析报错，可采取如下解决思路：

- 确定问题原因（❗ 非常重要，可据此快速搜索相关解决办法）
- 搜索、尝试解决办法，逐一排查
- 总结方法

### 解析报错提示：

- `parsing error: cannot find module '@babel/preset-env'`

### 确定原因

1. 原因一：安装包缺失
2. 原因二：VS Code-Eslint 默认不支持项目内嵌文件夹中的 node-modules
   ❗ 注意：

- 如果项目为使用 Next.js, Sanity 前后端初始化自动生成的文件夹，可排除原因一。
- 如果尝试原因一解决办法后未解决，亦可排除原因一

### 1. 原因一解决办法

#### 1. 重新下载安装包：`npm install --save-dev @babel/preset-env`

- 参考资料：
  - StackOverflow:
  - NPM 官网：[NPM：@babel/preset-env](https://www.npmjs.com/package/@babel/preset-env)；
  - Babel 官网：
  - CSDN：

### 原因二解决办法：

- 报错原因：VS Code-Eslint 默认不支持 Sanity 内嵌文件夹中的 package.json 配置
- 解决办法：在/.vscode > settings 中将项目文件夹和 Sanity 后台内嵌文件夹同时设置为工作文件夹
- 解决步骤：
  - 根目录新建 /.vscode 文件夹 => 新建 settings.json 文件
  - 在 settings.json 文件中，将项目文件夹和 Sanity 后台内嵌文件夹同时设置为工作文件夹

```tsx
{
	"eslint.workingDirectories": ["./Medium-Clone-v2", "./medium-clone-v2"]
}
```

- 参考资料：
