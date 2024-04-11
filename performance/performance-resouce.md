---
title: Performance Optimization Resource
topic: 
type: 
DateReviewed: 
reviewed: 
difficulty: 
comment: 
Type: S
tags:
  - Performance
DateDo: 
DateDone: 
DateDue: 
status: 
DateStarted: 2023-11-29
DateModified: 2024-04-11
aliases:
  - Performance Optimization Resource
---
# Performance Optimization Resource
## Reference
#### 1. Books
- [Web-performance-action/](http://www.allitebooks.in/web-performance-action/)
	- 这本书目前国内没有卖的。你可以看电子版本，我觉得是一本很不错的书，其中有 CSS、图片、字体、JavaScript 性能调优等
- [Designing for Performance by Lara Callender Hogan](https://designingforperformance.com/)
	- 这本在线的电子书很不错，其中讲了很多网页优化的技术和相关的工具，可以让你对整体网页性能优化有所了解。
- [高性能JavaScript](https://book.douban.com/subject/5362856/)
	- *High Performance JavaScript* ，这本书在国内可以买到，能让你了解如何提升各方面的性能，包括代码的加载、运行、DOM 交互、页面生存周期等。
	- 雅虎的前端工程师尼古拉斯·扎卡斯（Nicholas C. Zakas）和其他五位 JavaScript 专家介绍了**页面代码加载的最佳方法和编程技巧**，来帮助你编写更为高效和快速的代码。你还会了解到构建和部署文件到生产环境的最佳实践，以及有助于定位线上问题的工具。
- [高性能网站建设指南（第二版） (豆瓣)](https://book.douban.com/subject/26411563/)
	- *High Performance Web Sites: Essential Knowledge for Front-End Engineers* ，这本书国内也有卖，翻译版为《高性能网站建设指南：前端工程师技能精髓》。
	- 作者给出了 **14 条具体的优化原则**，每一条原则都配以**范例**佐证，并提供了在线支持。
	- 全书内容丰富，主要包括
		- 减少 HTTP 请求、
		- Edge Computing 技术、
		- Expires Header 技术、
		- gzip 组件、
		- CSS 和 JavaScript 最佳实践、
		- 主页内联、Domain 最小化、JavaScript 优化、避免重定向的技巧、删除重复 JavaScript 的技巧、关闭 ETags 的技巧、Ajax 缓存技术和最小化技术等。
- [Why does speed matter?](https://web.dev/i18n/en/why-speed-matters/)
	- Google 的 Web Fundamentals 里的 Performance  这一章节也有很多非常不错的知识和经验。
#### 2. Best Practice Documents
- [PageSpeed Insights 规则  |  Google Developers](https://developers.google.com/speed/docs/insights/rules?hl=zh-cn)
	- 谷歌给的一份性能指南和最佳实践
- [Best Practices for Speeding Up Your Web Site - Yahoo Developer Network](https://developer.yahoo.com/performance/rules.html?guccounter=1&guce_referrer=aHR0cHM6Ly90aW1lLmdlZWtiYW5nLm9yZy9jb2x1bW4vYXJ0aWNsZS8xMjM4OQ&guce_referrer_sig=AQAAALH986SMFo8PRsLKo0gI0veCV-WMlJ3a_UUkB-WITBCneHLteflIQb3v1vOc5BH6NyWnrvYj_tGiEYiS4CwuiwCc8JJh2zA1ybpSea32158ZppkSRjxkGT5SBVNpwtClCBWMwYct0MrLRHgMz120UHTrJZRXRtJ4x5oOA4lw4hX9)
	- 雅虎公司给的一份 7 个分类共 35 个最佳实践的文档。
#### 3. 性能优化的案例学习网站
- [WPO Stats](https://wpostats.com/)
	- ⭐重点推荐，WPO 是 Web Performance Optimization 的缩写，这个网站上有很多很不错的性能优化的案例分享，一定可以帮助你很多。
#### 4. Blogs and Cases
- [A Simple Performance Comparison of HTTPS, SPDY and HTTP/2 | HttpWatch BlogHttpWatch Blog](http://blog.httpwatch.com/2015/01/16/a-simple-performance-comparison-of-https-spdy-and-http2/)
	- 这是一篇比较浏览器的 HTTPS、SPDY 和 HTTP/2 性能的文章，除了比较之外，还可以让你了解一些技术细节。
- [7 Tips to Improve HTTP2 Performance | NGINX](https://www.nginx.com/blog/7-tips-for-faster-http2-performance/)
	- 对于 HTTP/2 来说，Nginx 公司给出的 7 个增加其性能的小提示。
- [Reducing Slack’s memory footprint - Slack Engineering](https://slack.engineering/reducing-slacks-memory-footprint/)
	- Slack 团队减少内存使用量的实践
- [Driving user growth with performance improvements | by Pinterest Engineering | Pinterest Engineering Blog | Medium](https://medium.com/pinterest-engineering/driving-user-growth-with-performance-improvements-cfc50dafadd7)
	- Pinterest 关于性能调优的一些分享，其中包括了前后端的一些性能调优实践。其实也是一些比较通用的玩法，这篇文章主要是想让前端的同学了解一下如何做整体的性能调优。
- [10 Javascript Performance Boosting Tips from Nicholas Zakas | Jon Raasch's Blog](http://jonraasch.com/blog/10-javascript-performance-boosting-tips-from-nicholas-zakas)
	- 10 个提高 JavaScript 运行效率的小提示，挺有用的。
- [Dev.Opera — Native Responsive Images](https://dev.opera.com/articles/native-responsive-images/)
	- Responsive 布局所带来的一些负面的问题。主要是图像适配的问题
- *Improve Page Load Times With DNS Prefetching* 
	- 这篇文章教了你一个如何降低 DNS 解析时间的小技术——DNS prefetching。
- [Jank busting for better rendering performance](https://web.dev/speed-rendering/)
	- Google I/O 上的分享，关于前端动画渲染性能提升。
- [Chrome DevTools - Chrome Developers](https://developer.chrome.com/docs/devtools/)
	- ⭐谷歌官方教你如何使用 Chrome 的开发工具来分析 JavaScript 内存问题的文章。
#### 5. Performance Tools
>接下来是一些性能工具。在线性能测试分析工具太多，这里只推荐比较权威的。

- [Make the Web Faster  |  Google Developers](https://developers.google.com/speed?hl=zh-cn)
	- 谷歌有一组 PageSpeed 工具来帮助你分析和优化网站的性能。Google 出品的，质量相当有保证。
- [GitHub - marcelduran/yslow: YSlow analyzes web pages and suggests ways to improve their performance based on a set of rules for high performance web pages.](https://github.com/marcelduran/yslow)
	- 雅虎的一个网页分析工具。
- [GTmetrix | Website Performance Testing and Monitoring](https://gtmetrix.com/)
	- 将 PageSpeed 和 YSlow 合并起来的一个网页分析工具，并且加上一些 Page load 或是其它的一些分析。也是一个很不错的分析工具。
- [GitHub - davidsonfellipe/awesome-wpo: A curated list of Web Performance Optimization. Everyone can contribute here!](https://github.com/davidsonfellipe/awesome-wpo)
	- 在 GitHub 上的这个 Awesome 中，你可以找到更多的性能优化工具和资源。
#### 6. JS 链接提速——国内
>中国的网络有各种问题（你懂的），所以，你不能使用 Google 共享的 JavaScript 链接来提速，你得用中国自己的。你可以到这里看看中国的共享库资源
- [Forget Google and Use These Hosted JavaScript Libraries in China - SEO Shifu Blog](https://chineseseoshifu.com/blog/china-hosted-javascript-libraries-jquery-dojo-boostrap.html)

[^1]: [企业级实战思路 - 什么是亮点 | 大圣前端进阶指南](https://shengxinjing.cn/react/arch/01.arch.html)





