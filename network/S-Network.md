### S-Network 
#### Protocols Basics
- [Web性能权威指南 (豆瓣)](https://book.douban.com/subject/25856314/)
	- *High Performance Browser Networking* 本书是谷歌公司高性能团队核心成员的权威之作，堪称**实战经验与规范解读完美结合的产物**。本书目标是涵盖 Web 开发者技术体系中应该掌握的所有**网络及性能优化**知识。全书以性能优化为主线，从 TCP、UDP 和 TLS 协议讲起，解释了如何针对这几种协议和基础设施来优化应用。然后深入探讨了无线和移动网络的工作机制。最后，揭示了 HTTP 协议的底层细节，同时详细介绍了 HTTP 2.0、 XHR、SSE、WebSocket、WebRTC 和 DataChannel 等现代浏览器新增的能力。
#### HTTP/2
> [HTTP/2 - Wikipedia](https://en.wikipedia.org/wiki/HTTP/2) 也是 HTTP 的一个新的协议，于 2015 年被批准通过，现在基本上所有的主流浏览器都默认启用这个协议。所以，你有必要学习一下这个协议
- [http2 explained - The HTTP/2 book](https://daniel.haxx.se/http2/)
- [HTTP2\_White\_Paper\_v4.pdf](https://www.nginx.com/wp-content/uploads/2015/09/NGINX_HTTP2_White_Paper_v4.pdf)
- HTTP/2 的两个 RFC：
	- [RFC 7540 - Hypertext Transfer Protocol Version 2 (HTTP/2)](https://httpwg.org/specs/rfc7540.html) 
		- HTTP/2 的协议本身
	- [RFC 7541 - HPACK: Header Compression for HTTP/2](https://httpwg.org/specs/rfc7541.html)
		- HTTP/2 的压缩算法
#### Web Socket
>新的 HTML5 支持 [WebSocket - Wikipedia](https://en.wikipedia.org/wiki/WebSocket)，所以，这也是你要学的一个重要协议。
- [WebSocket官方文档翻译——HTML5 Web Sockets:A Quantum Leap in Scalability for the Web\_丨知耻而后勇丨的博客-CSDN博客](https://blog.csdn.net/u013252773/article/details/24228375)
	- [Taking a Quantum Leap with Html 5 WebSocket](https://www.slideshare.net/velvetflair/taking-a-quantum-leap-with-html-5-websocket)
	- 这篇文章比较了 HTTP 的几种链接方式，Polling、Long Polling 和 Streaming，并引入了终级解决方案 WebSocket。你知道的，了解一个技术的缘由是非常重要的。
- [javascript - My Understanding of HTTP Polling, Long Polling, HTTP Streaming and WebSockets - Stack Overflow](https://stackoverflow.com/questions/12555043/my-understanding-of-http-polling-long-polling-http-streaming-and-websockets)
	- 这是 StackOverflow 上的一个 HTTP 各种链接方式的比较，也可以让你有所认识。
- [How to WebSockets [Complete Guide] | Treehouse Blog]( https://blog.teamtreehouse.com/an-introduction-to-websockets )
	- 一个 WebSocket 的简单教程。
- [GitHub - facundofarias/awesome-websockets: A curated list of Websocket libraries and resources.](https://github.com/facundofarias/awesome-websockets)
	- GitHub 的 Awesome 资源列表。
- 一些和 WebSocket 相关的想法，可以开阔你的思路
	- [Introducing WebSockets - Bringing Sockets to the Web](https://web.dev/websockets-basics/)
	- [Websockets 101 | Armin Ronacher's Thoughts and Writings](https://lucumr.pocoo.org/2012/9/24/websockets-101/)
	- [The State of Real-Time Web in 2016 - by Paul Banks](https://banksco.de/p/state-of-realtime-web-2016.html)
	- [WebSockets, caution required!](https://samsaffron.com/archive/2015/12/29/websockets-caution-required)
## 学习建议  
1计算机网络的理论知识较多，初学不建议啃教材或者专业书籍，而是通过一些趣味科普书籍或视频来逐步了解。  
2建议和写文章一样，从整体到局部去学计算机网络，先了解有哪些网络分层、每个层次的作用和联系，再去按序了解每个层次内部的协议和细节。  
3计算机网络知识不要去死记硬背，哪怕记不住也没关系，等自己开发程序的时候可以思考数据传输的过程（比如网站加载的过程），通过抓包等实操的方式来加深印象。  
4不从事网络相关工作的话，计算机网络不用学的很深入，学习完重点知识就够了，甚至直接通过看面试题去学习也完全没有关系。  
5如果要从事网络相关工作（比如网络工程师），建议去考一些认证，比如华为认证、思科认证等等，可以自行了解一下。  
## 计算机网络学习路线  
建议大家按照以下 3 个阶段来学习：  
1基础学习  
2实际运用  
3备战面试  
### 一、基础学习  
急于求职的话，本阶段可跳过  
本阶段的目标：了解计算机网络基础知识，跟着一个视频或书籍过一遍，对网络分层模型和重点知识有个大致的印象即可。 
自学网络可能会比较枯燥，建议先看看有趣的课外书，比如《图解 HTTP》，当个睡前读物即可。  
正式学习网络的话，如果目标是求职，可以看《计算机网络微课堂》视频课来入门。如果目标是考研升学，还在学校的同学好好上课一般就没问题了，自学的话可以看《王道计算机考研 - 计算机网络》视频，也可以阅读《计算机网络 - 自顶向下方法》或《计算机网络 - 谢希仁》等书籍。  
后面要面试前，再重点去背一些八股文就行。  
#### 推荐资源  
●视频  
○⭐ 计算机网络微课堂：https://www.bilibili.com/video/BV1c4411d7jb（强烈推荐）  
○王道计算机考研 - 计算机网络：https://www.bilibili.com/video/BV19E411D78Q（适合考研）  
○中科大郑烇、杨坚全套《计算机网络（自顶向下方法 第7版）》：https://www.bilibili.com/video/BV1JV411t7ow（适合考研、学术）  
○中国大学 MOOC 哈工大计算机网络课程：[https://www.icourse163.org/course/HIT-154005](https://www.icourse163.org/course/HIT-154005)  
●书籍  
●⭐️ 小林的图解网络：[https://pan.baidu.com/s/1D6ygpsrZbEKK9V-Z80xcvQ](https://pan.baidu.com/s/1D6ygpsrZbEKK9V-Z80xcvQ) 提取码: ecf2（号主原创，质量很高）  
○⭐《图解 HTTP》：[https://www.aliyundrive.com/s/HifozcgJwep](https://www.aliyundrive.com/s/HifozcgJwep) 提取码: 9gc7  
○⭐《图解 TCP / IP》：[https://www.aliyundrive.com/s/XYyAymeeXRy](https://www.aliyundrive.com/s/XYyAymeeXRy) 提取码: 9gc7  
○《网络是怎样连接的》：[https://www.aliyundrive.com/s/3FgCbvHGQQZ](https://www.aliyundrive.com/s/3FgCbvHGQQZ) 提取码: 9gc7  
○《计算机网络（第 7 版）》 谢希仁：[https://www.aliyundrive.com/s/3VsnQoKqxdi](https://www.aliyundrive.com/s/3VsnQoKqxdi) 提取码: 9gc7  
○《计算机网络 - 自顶向下方法（第 6 版）》：[https://www.aliyundrive.com/s/Dc3itcB6GU9](https://www.aliyundrive.com/s/Dc3itcB6GU9) 提取码: 9gc7（大黑书，难度比较大，一般不推荐）  
●大学课件  
○浙大计算机网络基础：[https://github.com/QSCTech/zju-icicles](https://github.com/QSCTech/zju-icicles)  
### 二、实际运用  
本阶段可跳过，在开发中实践即可  
本阶段的目标：根据自己的职业发展方向进行不同的实践，运用和巩固计算机网络知识。  
比如：  
1后端开发：基于 Socket 开发自己的通讯应用 / 框架、实现自己的浏览器、阅读开发框架源码等  
2前端开发：使用 HTTPS 协议增加网站安全性、使用 HTTP 2 协议提高网站加载速度、使用控制台等抓包工具分析请求 / 响应  
3网络工程师：使用华为 eNSP 或 Cisco Packet Tracer 模拟器搭建网络拓扑并进行配置  
4安全工程师：使用 Wireshark 之类的抓包工具分析数据包 / 数据帧  
### 实验  
●《计算机网络－自顶向下方法（第 6 版）》编程作业：[https://github.com/moranzcw/Computer-Networking-A-Top-Down-Approach-NOTES](https://github.com/moranzcw/Computer-Networking-A-Top-Down-Approach-NOTES)  
●《计算机网络 - 自顶向下方法》习题 / 编程 / 实验答案：[https://github.com/jzplp/Computer-Network-A-Top-Down-Approach-Answer](https://github.com/jzplp/Computer-Network-A-Top-Down-Approach-Answer)  
●哈工大计算机网络实验：[https://github.com/rccoder/HIT-Computer-Network](https://github.com/rccoder/HIT-Computer-Network)  
### 网络相关认证  
●华为 HCIA-HCIP-HCIE router&switch 视频教程：[https://t.zsxq.com/FEiaEEA](https://t.zsxq.com/FEiaEEA)  
●H3C 厂商认证资料（面试+笔记+电子书+培训课件+实验手册+产品资料）：[https://t.zsxq.com/NBAQRZ3](https://t.zsxq.com/NBAQRZ3)  
### 三、备战面试  
面试时对计算机网络的考察主要有 5 种形式（主要针对前后端开发）：  
1直接问你某个具体的知识点，比如：讲解 TCP 三次握手和四次挥手机制  
2结合不同方向的专业知识来考察，比如：谈谈网站的加载过程（前端）、聊聊四七层负载均衡的实现和优缺点（后端）  
3通过实际开发中遇到的问题考察你的网络基础，比如：网站加载过慢，有哪些优化方式？  
4问你某个框架（轮子）的核心设计和源码细节，可能会包含计算机网络知识点的运用，比如 Netty 针对 UDP 协议的封装设计  
5系统设计类问题，比如：如何实现一个浏览器？（这种问题相对比较少）  
### 资源  
#### 总结复习  

●⭐️ 牛客网计算机网络基础在线练习：https://www.nowcoder.com/exam/intelligent（随缘刷刷就行，绝大多数题目面试不会问）  
●软件设计师计算机网络考点：[https://pan.baidu.com/s/1K1hpKuS6XGG71jWr4N3UCg](https://pan.baidu.com/s/1K1hpKuS6XGG71jWr4N3UCg) 提取码: 2g55  
●软件设计师计算机网络基础知识：[https://pan.baidu.com/s/1XJzDJcxRhqs360nw-T8VA](https://pan.baidu.com/s/1XJzDJcxRhqs360nw-_T8VA) 提取码: cs81  
#### 面试题  
●⭐️ 阿秀的 100+ 计算机网络面试题汇总：[https://interviewguide.cn/#/Doc/Knowledge/计算机网络/计算机网络](https://interviewguide.cn/#/Doc/Knowledge/%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C/%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C)  
●计算机网络 97 问：[https://www.nowcoder.com/discuss/807702](https://www.nowcoder.com/discuss/807702)  
●25 道计算机网络面试题总结：[https://blog.csdn.net/lxw1844912514/article/details/120279006](https://blog.csdn.net/lxw1844912514/article/details/120279006)  
●20 道计算机网络面试题总结：[https://www.nowcoder.com/discuss/839894](https://www.nowcoder.com/discuss/839894)
●计算机网络基础面试宝典：[https://pan.baidu.com/s/1whsPlPyDnQGf8uH5sV4Awg](https://pan.baidu.com/s/1whsPlPyDnQGf8uH5sV4Awg) 提取码: 5j4n  
●13 道计算机网络面试题：[https://pan.baidu.com/s/1Ou_aEWq4o7cfoz1TY126TA](https://pan.baidu.com/s/1Ou_aEWq4o7cfoz1TY126TA) 提取码: 8uru  




