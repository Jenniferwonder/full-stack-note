---
DateStarted: 2023-08-22
DateModified: 2024-04-17
---
### 介绍

很多同学第一次接触 Redis 可能都是因为 “缓存”，也有很多同学误以为 Redis 就是缓存、只能做缓存。  
事实上，Redis 是知名的高性能内存 K / V 存储系统，除了缓存之外，Redis 还可以用作配置存储、消息队列、解决分布式一致性问题等。正因为 Redis 的高性能、通用性、易用性、功能强大，使得它成为了后端开发中必不可少的中间件。  
只要你的学习方向是后端开发，就必须要系统地学习 Redis。不仅要学会应用到项目中，还要学习它优秀的系统设计以及实现原理，可以开拓我们开发程序、解决问题的思路。

### 学习条件

1 目标方向是后端开发或数据库、数据开发相关的岗位（前端同学先不要学了）  
2 先学完一套开发框架（比如 SSM、SpringBoot），再学习 Redis

### 学习路线

建议大家按照以下五个阶段来学习：  
1 基础入门  
2 实战应用  
3 高阶知识  
4 底层原理  
5 备战面试

### 大纲

![](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/Redis.png)

### 知识点

#### ● 一、基础入门

○Redis 是什么？  
○SQL 和 NoSQL  
○Redis 特点  
○Redis 安装  
○ 连接方式  
○ 常用命令  
■ 通用命令  
■ 命令手册  
○ 基本数据结构  
■String  
■Hash  
■List  
■Set  
■SortedSet  
○Redis 管理工具  
■Redis Insight  
■Quick Redis  
■RESP  
○Redis 客户端及用法  
■Jedis  
■Spring Data Redis  
■Redisson  
■Lettuce

#### ● 二、实战应用

○ 分布式 Session  
○ 高级数据结构  
■GEO（地理位置计算）  
■Bitmap（实现签到）  
■HyperLogLog（实现 U / V 统计）  
■Bloom Filter  
■ 消息队列  
●Pub/Sub  
●Stream  
○ 缓存  
■ 缓存更新  
●Cache Aside 模式  
●Read / Write Through 模式  
●Write Behind 模式  
■ 缓存问题及解决方案  
● 缓存穿透  
● 缓存击穿  
● 缓存雪崩  
■ 多级缓存  
■ 缓存预热  
○ 分布式全局唯一 id 生成  
○Lua 脚本（实现秒杀）  
○ 分布式锁 Redisson 实现  
○Feed 流实现  
○ 事务

#### ● 三、高阶知识

○Redis 最佳实践  
■ 键值设计  
■ 客户端优化  
■ 服务端优化  
○ 数据持久化  
■RDB  
■AOF  
■ 两者对比  
○ 主从同步  
■ 全量同步  
■ 增量同步  
■ 主从集群优化  
○ 哨兵集群  
■ 介绍和特点  
■ 故障转移  
○ 分片集群  
■ 介绍和特点  
■ 散列插槽  
■ 集群伸缩  
■ 故障转移  
■ 数据迁移

#### ● 四、底层原理

○ 底层数据结构  
■ 动态字符串  
■IntSet  
■Dict  
■ZipList  
■SkipList  
■Redis Object  
■ 五种基本数据结构的底层  
○Redis 网络模型  
■ 阻塞 I / O  
■ 非阻塞 I / O  
■I / O 多路复用  
○Redis 线程模型  
○Redis 通信协议  
○Redis 内存淘汰策略

#### ● 五、备战面试

### 学习资源

#### 1、入门教程（从这里开始）

直接看这套视频课程即可一条龙入门：[https://www.bilibili.com/video/BV1cr4y1671t](https://www.bilibili.com/video/BV1cr4y1671t)  
几乎包括了 Redis 所有入门知识和主流应用、还有高级用法和原理的讲解，强烈推荐。  
除了视频学习之外，还可以配合《图解 Redis》文档食用：[https://xiaolincoding.com/redis/](https://xiaolincoding.com/redis/)

#### 2、项目实战

Redis 项目推荐及笔记：[https://t.zsxq.com/07JMnQvne](https://t.zsxq.com/07JMnQvne)

#### 3、可视化工具

Redis Insight：[https://redis.io/docs/stack/insight/](https://redis.io/docs/stack/insight/)  
Quick Redis：[https://quick123.net/](https://quick123.net/)

#### 4、命令手册

Redis 官网命令集：[https://redis.io/commands/](https://redis.io/commands/)（命令忘了就查）  
中文版命令集：[http://www.redis.cn/commands.html](http://www.redis.cn/commands.html)

#### 5、经典面试题

视频 1：[https://www.bilibili.com/video/BV1Ni4y1Q7XM/](https://www.bilibili.com/video/BV1Ni4y1Q7XM/)  
视频 2：[https://www.bilibili.com/video/BV1BB4y1y7M2](https://www.bilibili.com/video/BV1BB4y1y7M2)  
视频 3：[https://www.bilibili.com/video/BV1it4y1W7D1](https://www.bilibili.com/video/BV1it4y1W7D1)  
常见面试题整理（by 小林）：[https://xiaolincoding.com/redis/base/redis_interview.html](https://xiaolincoding.com/redis/base/redis_interview.html)

### 学习建议

1Redis 是一个注重实际运用的技术，在学习 Redis 的过程中，要记得多敲命令 / 多写代码来操作 Redis，将 Redis 实际运用到你之前做过的项目中，而不是死记硬背。尤其是不要去背命令和代码，忘了就查、多写几次后印象自然就深刻了。  
2 对于初学后端的同学来说，学完第二阶段（实战应用）后就可以再去学消息队列、微服务等其他知识了。等主流的后端开发技术都会用后、面试前再回过头来补高级知识和原理即可。  
3Redis 的最佳实践部分要重点学习，建议是整理笔记便于自己复习查阅。争取养成好的设计和编码习惯，对以后的工作发展会很有帮助。
学会如何简单地使用缓存并不难，和数据库类似，无非就是调用 API 对数据进行增删改查。  
因此，建议先能够独立使用它，了解缓存的应用场景；再学习如何在 Java 中操作缓存中间件，并尝试和项目相结合，提高系统的性能。  
跟着视频教程实操一遍即可，可以等到面试前再去深入了解原理和高级特性。

### 经典面试题

1Redis 为什么快？  
2Redis 有哪些常用的数据结构？  
3Redis RDB 和 AOF 持久化的区别，如何选择？  
4 如何解决缓存击穿、缓存穿透、雪崩问题？  
5 如何用 Redis 实现点赞功能，怎么设计 Key / Value？

### 资源

#### ● 视频

○⭐ 2022 黑马 Redis 从基础到原理：[https://www.bilibili.com/video/BV1cr4y1671t](https://www.bilibili.com/video/BV1cr4y1671t)（结合项目去讲，强烈推荐）  
○ 尚硅谷 - 2021 最新 Redis 6 入门到精通教程：[https://www.bilibili.com/video/BV1Rv41177Af](https://www.bilibili.com/video/BV1Rv41177Af) （基于 Redis 6 的，推荐）

#### ● 文档

○Redis 命令参考：[http://redisdoc.com/](http://redisdoc.com/)  
○Redis 面试题整理：[https://github.com/lokles/Web-Development-Interview-With-Java/blob/main/Redis 问题.md](https://github.com/lokles/Web-Development-Interview-With-Java/blob/main/Redis%E9%97%AE%E9%A2%98.md)

#### ● 书籍

○《Redis 实战》（经典）

#### ● 工具

○⭐ Redis 在线练习：[https://try.redis.io/](https://try.redis.io/) （强烈推荐）
