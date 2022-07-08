# interview
记录2022年找工作的一些题目

## 20220705 滴滴
### 算法
单向链表的翻转
### mysql：
怎么做数据库的分库分表，什么情况下进行分库分表
主从复制步骤，主库从库延时超过1S怎么做？
什么情况会引发索引失效？
慢sql
### redis：
缓存淘汰策略是否有了解
都哪些场景用到了缓存
### 消息中间件
rockemq怎么保证消息的可靠性
### 操作系统
进程、线程、协程的区别，goroutine是什么
### go
slice是怎么扩容的
make和new的区别
go语言是怎么处理panic的？http://c.biancheng.net/view/63.html
为什么Goroutine不需要上下文切换。goroutine和线程的区别。
### 项目
项目中遇到的比较难解决的问题


## 20220708 晋江

### PHP试题
当论坛帖子数量十分庞大时，直接使用MySQL limit查询进行分页会变得十分缓慢，因此我们需要使用其他技术辅助进行分页处理。
假如我们帖子列表和发帖都是用Ajax的POST来提交数据的，请用PHP，并且结合MySQL和redis的ZSET编写程序，实现以下基本逻辑：
1、处理获取帖子列表页内容的AJax请求，AJax请求的参数为page(页码)，程序需要返回当前页码的所有帖子的数据，返回的数据类型是json格式的，请自行规定具体接口数据结构。
2、处理发表帖子的Ajax post请求，实现把数据写入到MYSQL等操作。
#### 具体需求如下：
1、分页是按发帖时间倒序排列，每页50条；
2、不允许使用开源框架；
3、进行必要的封装；
4、假设Redis和MySQL服务器使用localhost，用户名及密码均为www.jjwxc.net；
5、代码结构良好，PhpDoc注释清晰；

#### 论坛表中主贴表（board）主要字段如下：
字段	类型	注释
Id	int(11)	 主贴id
subject	varchar(100)	 标题
Author	varchar(20)	 发帖人
Idate	datetime	 发帖时间
Replies	int(11)	 回帖数量
Body	text	 主贴内容
Ndate	datetime	 最新回复时间
Ip	varchar(15)	 
……		

