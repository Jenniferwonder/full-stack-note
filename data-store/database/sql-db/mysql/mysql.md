## 大纲  
对数据库的学习主要分为 4 部分：  
1数据库理论  
2MySQL 入门及实践  
3SQL 语句  
4MySQL 高级（原理）  
一般对绝大多数同学来说，把前 3 部分学完就足够了，高级部分面试会考察一些，背背八股文面试题就行。  
其中，最最最重要的是一定要能根据业务场景独立设计库表，并且熟练编写 SQL 语句。  
## 一、数据库理论  
以前在大学的时候，老师是先给我们讲理论，再上手写代码实践的。但是现在网上很多的教程都是带着大家边实践边讲理论，我觉得这种方式更好，能让大家更轻松地快速入门、不枯燥。  
入门可以看这个视频教程：[https://www.bilibili.com/video/BV1Kr4y1i7ru](https://www.bilibili.com/video/BV1Kr4y1i7ru) ，只用看 P1 - P57 集就足够了。  
可以搭配菜鸟教程的 MySQL 文档进行巩固和实操：[https://www.runoob.com/mysql/mysql-tutorial.html](https://www.runoob.com/mysql/mysql-tutorial.html)（文档中的 PHP 代码部分可忽略）  
### 知识点  
● 数据库基本概念  
○数据库  
■关系型数据库  
■非关系型数据库  
○数据库管理系统  
○表  
○字段  
○视图  
○约束  
○SQL  
○查询  
○索引  
○事务  
○主键  
○外键  
○语法分类  
■DDL  
■DML  
■DCL  
■DQL  
● 数据库设计  
○数据库三大范式  
○表关联  
■1 对 1  
■1 对多  
■多对多  
■笛卡尔积  
○E-R 图  
### 资源  
以下资源仅供参考和查漏补缺，有选择地观看即可。  
#### 在线练习  
○⭐ SQL 自学网：[http://xuesql.cn/](http://xuesql.cn/)  
○⭐ SQL 在线运行：[https://www.bejson.com/runcode/sql/](https://www.bejson.com/runcode/sql/)  
#### 文档  
○SQL - 菜鸟教程：[https://www.runoob.com/sql/sql-tutorial.html](https://www.runoob.com/sql/sql-tutorial.html)  
○MySQL - 菜鸟教程：[https://www.runoob.com/mysql/mysql-tutorial.html](https://www.runoob.com/mysql/mysql-tutorial.html)  
#### 网站  
○[数据库大全](https://www.code-nav.cn/rd/?rid=b00064a76012546b016e274a3724c5f0)：果创云收录的各种数据库表设计
#### 视频：  
○⭐ 2022 黑马 MySQL 教程：[https://www.bilibili.com/video/BV1Kr4y1i7ru](https://www.bilibili.com/video/BV1Kr4y1i7ru)（倾向于速成，初学只看完 P57 节前的基础篇即可，后面可以再来补进阶知识）  
○老杜 - mysql入门基础 + 数据库实战：[https://www.bilibili.com/video/BV1Vy4y1z7EX](https://www.bilibili.com/video/BV1Vy4y1z7EX) （内容相对精炼，有习题）  
○尚硅谷 - MySQL基础教程：[https://www.bilibili.com/video/BV1xW411u7ax](https://www.bilibili.com/video/BV1xW411u7ax) （小姐姐讲课，但感觉音质一般）  
●老杜 MySQL 入门基础 + 数据库实战：[https://www.bilibili.com/video/BV1Vy4y1z7EX](https://www.bilibili.com/video/BV1Vy4y1z7EX) （内容相对精炼，有习题）  
●尚硅谷 MySQL 基础到高级：[https://www.bilibili.com/video/BV1iq4y1u7vj](https://www.bilibili.com/video/BV1iq4y1u7vj) （近 22 年的课，质量也还不错）  
●尚硅谷 - MySQL基础教程：[https://www.bilibili.com/video/BV1xW411u7ax](https://www.bilibili.com/video/BV1xW411u7ax) （小姐姐讲课，但感觉音质一般）  
#### 书籍：  
●《MySQL 即学即用》：[https://book.douban.com/subject/36230167/](https://book.douban.com/subject/36230167/)  
●《MySQL是怎样使用的，快速入门MySQL》：[https://book.douban.com/subject/35670862/](https://book.douban.com/subject/35670862/)  
## 二、MySQL 入门及实践  
这个阶段和上个阶段是可以一起学习的，就看上面说的教程即可。  
本阶段先了解 MySQL 的基本用法，能够通过 MySQL 控制台或可视化工具来操作数据库。然后就可以去看其他的教程，用你熟悉的编程语言去操作数据库了，比如 Java 的 JDBC 或 MyBatis 框架；在学习过程中，建议多尝试自己设计库表，培养良好的数据库设计能力。  
当你要自己设计数据库时，可以看看 [数据库大全](https://www.code-nav.cn/post/1607270258404503553) 这个网站，里面有很多的案例可供学习参考。  
### 知识点  
●MySQL 安装  
●MySQL 常用命令  
●MySQL 基本操作  
○插入数据  
○删除数据  
○修改数据  
○查询数据  
●MySQL 关键字  
●MySQL 函数  
●MySQL 查询语法  
○基本查询  
○条件查询  
○聚合查询  
○分组查询  
○连接  
■内连接  
■外连接  
○子查询  
○组合查询  
●MySQL 约束  
●MySQL 存储引擎  
○游标  
●MySQL 触发器  
●MySQL 事务  
●MySQL 索引  
●MySQL 视图  
●MySQL 库表设计  
●客户端操作（比如 Java）  
## 三、SQL 语句  
对后端开发和数据开发来说，SQL 都是一个核心技能。  
很多速成的同学可能只会使用框架来操作数据库，缺少了自己编写 SQL 的能力。所以这里建议大家先把以下知识点中的 SQL 语法都尝试编写执行一遍，然后在平时开发系统时多写多练、熟能生巧，而不是死记硬背。  
可以通过以下网站在线练习 SQL：  
●牛客网 SQL 题库：[https://www.nowcoder.com/exam/intelligent?questionJobId=10&tagId=21015](https://www.nowcoder.com/exam/intelligent?questionJobId=10&tagId=21015) （在本页面最底下）  
●SQL 自学网：[http://xuesql.cn/](http://xuesql.cn/)  
●SQL 在线运行：[https://www.bejson.com/runcode/sql/](https://www.bejson.com/runcode/sql/)  
●SQL - 菜鸟教程：[https://www.runoob.com/sql/sql-tutorial.html](https://www.runoob.com/sql/sql-tutorial.html)  
### 知识点  
●基本概念  
○什么是 SQL  
○不同数据库的 SQL 差异  
●基础语法  
○选择 select  
■select *  
■select field  
■select field as xxx  
○排序 order by  
○条件查询 where  
■and  
■or  
■not  
■like  
■is null / is not null  
○去重 distinct  
○截断 limit  
○分页 offset  
○分支 case when  
●分组聚合 group by  
○单级  
○多级  
○having 子句  
●函数  
○时间函数  
○字符串函数  
○聚合函数  
○开窗函数  
■sum over  
■sum over order  
■lag、lead  
■row number  
●关联查询  
○where  
○join  
○left join  
○right join  
○outer join  
●子查询  
●组合查询  
○union  
○union all  
## MySQL 高级  
如果你是一名后端开发，还没有把框架学完、还不能独立开发完整项目，那么先不要学习这部分知识。  
不过对于一名数据库管理员（数据库运维）来说，这部分知识是必学的！  
### 推荐几本不错的书籍：  
●《MySQL 是怎样运行的》：[https://book.douban.com/subject/35231266/](https://book.douban.com/subject/35231266/) （算是国产良心强作）  
●《高性能 MySQL》：[https://book.douban.com/subject/36096578/](https://book.douban.com/subject/36096578/) （领域经典，但是读起来可能会有一定难度）  
还有一些小实践，比如构建自己的数据库：[https://cstack.github.io/db_tutorial/](https://cstack.github.io/db_tutorial/)  
### 看视频的话就经典培训机构：  
●黑马：[https://www.bilibili.com/video/BV1Kr4y1i7ru](https://www.bilibili.com/video/BV1Kr4y1i7ru) （P58 - P195）  
●尚硅谷：[https://www.bilibili.com/video/BV1iq4y1u7vj](https://www.bilibili.com/video/BV1iq4y1u7vj) （P96 - P199）  
### 知识点  
●MySQL 体系架构  
●MySQL 执行原理  
●MySQL 并发控制  
●MySQL 事务隔离级别  
●MySQL 权限控制  
●MySQL 安全管理  
●MySQL 存储引擎  
○InnoDB  
○MyISAM  
●MySQL 数据文件  
●MySQL 锁  
○排他锁 / 共享锁  
○行锁 / 表锁  
○意向锁  
■意向共享锁  
■意向独占锁  
○间隙锁  
●MySQL 运维管理  
●MySQL 监控  
●MySQL 性能指标  
●MySQL 调优  
○软件层面优化  
○硬件层面优化  
○配置优化  
○索引优化  
○表和字段设计  
●数据备份与恢复  
●主从复制  
●读写分离  
●分库分表  
## 经典面试题  
列举一些数据库相关的高频考题（不到面试前一个月，不要急着背）：  
### 基础理论  
1什么是数据表、字段、主键、外键、视图？  
2什么是数据库的三大范式？  
### 事务和锁  
1什么是数据库事务？事务的 ACID 特性是什么？  
2并发事务的控制方式有哪些？  
3MySQL 事务有哪些隔离级别，分别有什么特点？  
4MySQL 事务的默认隔离级别是什么？  
5MySQL 事务的隔离级别是怎么实现的？  
6什么是 MVCC？InnoDB 引擎是如何实现 MVCC 机制的？  
7MySQL 中表级锁和行级锁有什么区别？各自有什么优缺点？  
8什么是数据库中的共享锁、排他锁？  
9是什么意向锁？它有什么作用？  
### 存储和索引  
1MySQL 支持哪些存储引擎？默认使用哪个？  
2MySQL 引擎中，MySIAM 和 InnoDB 有什么区别，各有什么优缺点，如何选择？  
3什么是数据库索引，使用索引有什么优缺点？  
4MySQL 中的索引是怎么实现的？  
5B+ 树是什么，B 树和 B+ 树有什么区别？为什么 MySQL 要用 B+ 树实现索引？  
6数据库索引有哪些类型？聚簇索引和非聚簇索引有什么区别，各有什么优缺点？  
7什么是索引下推，它有什么好处？  
8什么情况下数据库索引会失效？  
9什么是数据库索引的最左匹配原则？  
10你平时是怎么使用数据库索引的，有哪些高效利用索引的经验和技巧？  
### 实践操作  
1什么是存储过程？使用存储过程有哪些优缺点？  
2MySQL 有哪些日志？请分别介绍一下？  
3binlog 和 redolog 有什么区别？什么是两阶段提交？  
4什么是 undolog 日志？undolog 如何保证事务的原子性？  
5什么是 MySQL 的查询缓存，有什么优缺点？  
6如何对 MySQL 的数据进行备份和恢复？  
7什么是 MySQL 执行计划？如何获取执行计划并对其进行分析？  
8一条 SQL 语句在 MySQL 中的执行过程是怎样的？  
9以 MySQL 为例，有哪些数据库性能优化的方法？  
10如何定位 MySQL 慢查询？
企业中大部分业务数据都是用关系型数据库存储的，因此数据库是后台开发同学的必备技能，其中 MySQL 数据库是目前的主流，也是面试时的重点。  
  

### 知识  
  
●基本概念  
●MySQL 搭建  
●SQL 语句编写  
●约束  
●索引  
●事务  
●锁机制  
●设计数据库表  
●性能优化  
  

### 学习建议  
  
其中，SQL 语句编写 和 设计数据库表 这两个能力一定要有！  
  
比如让你做一个学生管理系统，你要能想到需要哪些表，比如学生表、班级表；每个表需要哪些字段、字段类型。  
  
这就要求大家多写 SQL、多根据实际的业务场景去练习设计能力。  
  

### 经典面试题  
  
1MySQL 索引的最左原则  
2InnoDB 和 MyIsam 引擎的区别？  
3有哪些优化数据库性能的方法？  
4如何定位慢查询？  
5MySQL 支持行锁还是表锁？分别有哪些优缺点？  
  
