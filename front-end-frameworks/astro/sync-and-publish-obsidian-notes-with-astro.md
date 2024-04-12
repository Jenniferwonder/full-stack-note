---
title: "Sync and Publish Obsidian Notes with Astro "
topic: 
type: 
tags:
  - Astro
DateStarted: 2024-04-07
DateModified: 2024-04-12
DateDo: 
DateDone: 
DateDue: 
DateReviewed: 
reviewed: 
difficulty: 
status: 
comment: 
aliases:
  - Sync and Publish Obsidian Notes with Astro
linter-yaml-title-alias: "Sync and Publish Obsidian Notes with Astro "
---
# Sync and Publish Obsidian Notes with Astro 
## Purpose
- [x] Public notes from different obsidian vaults keep in sync with public notes in Astro project using **mklink/ symlink** 
	- ✅Update stays in sync 
	- ✅Obsidian vault doesn't get bloated with `node_modules` and files other than notes
- [x] Astro supports for wikilink/ markdown link, so that notes can be managed by Obsidian 
	- ❌Manually copy notes to Astro, p.s. update link  
	- ❌Replace links by vscode 
	- ✅use wikilink-parser (wikilink can be recognized by Astro)
## For image links 
#### ❌ Local Images
wikilinks like `![[image.png]]` is unrecognizable in Astro, so change them to markdown link format `![image](image.png)` 
- replace empty space in image name to `-`
- replace `%20` in image markdown link to `-`
- add a `./` before the image link, like this `![](./z-Assets/image.png)`
#### 👍 Remote Images (using free pic-bed)

## For note links  
If using [astro-starlight](https://starlight.astro.build/getting-started/) template, the internal link to another markdown file has to be rewritten as `[another](../another)` so that the url param doesn't lead to `note/another` but `/another`, and wikilink `[[another.md]]` is unrecognizable. Neither approach is compatible for both Astro and Markdown editor like Obsidian.
#### ❌ Solutions I've tried
> neither of the following solution works in astro-starlight project

- [GitHub - vernak2539/astro-rehype-relative-markdown-links: Rehype Plugin for Astro that allows for usage of relative links between markdown files](https://github.com/vernak2539/astro-rehype-relative-markdown-links)
- [Getting Started | Starlight Links Validator](https://starlight-links-validator.vercel.app/getting-started/)

##### starlight-obsidian
>[GitHub - HiDeoo/starlight-obsidian: Starlight plugin to publish Obsidian vaults](https://github.com/HiDeoo/starlight-obsidian)


| Pros                              | Cons                                                                      |
| --------------------------------- | ------------------------------------------------------------------------- |
| ✅ Supports wikilink to astro-link | ❌ can only link to 1 obsidian vault (not able to publish multiple vaults) |
|                                   | ❌ a `Note` item in Sidebar can't be removed                               |
|                                   | ❌ duplicated notes in astro-project `public` folder (bloat disk space)    |
|                                   | <br><br>                                                                  |

#### 👍 Current solution I'm using
- [parsing - Using markdown wiki-links in Astro framework - Stack Overflow](https://stackoverflow.com/questions/76163067/using-markdown-wiki-links-in-astro-framework)
- @portaljs/remark-wiki-link

Turn note links into absolute path wikilink 
Configure `@portaljs/remark-wiki-link`















