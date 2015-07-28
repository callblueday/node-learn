- node是服务器程序，但没法像Apache一样，不是部署后就立即能启动和运行服务器
- 它是通过添加各种模块来完成各种服务支持。类似Apace添加一个php模块，允许开发人员创建动态web页
- node是事件驱动的编程，事件可以理解为一种状态的产生或者改变
- 它适用于处理高流量的应用程序
- 每个连接发射一个在 Node 引擎的进程中运行的事件，而不是为每个连接生成一个新的 OS 线程

- 最大的优点是内存消耗可控，设计好了可以不随流量而变化，因此可以在配置很差的服务器上提供高性能服务
- npm是node的一个特性，是一个内置功能，用于安装和管理node模块


node适合的
----------
在响应客户端之前，您预计可能有很高的流量，但所需的服务器端逻辑和处理不一定很多。它本质上只是从某个数据库中查找一些值并将它们组成一个响应。


node使用
--------
- node 在代码里定义好服务器监听端口，运行node，执行代码时，服务器被启动，默认可被访问地址是http:localhost，例如：定义的监听端口是83，则访问地址是：
http://localhost:83/，可以访问到该代码文件，在代码里定义输出结果，则可以在浏览器里得到展现。


入门认识：http://www.ibm.com/developerworks/cn/opensource/os-nodejs/index.html?ca=drs-


node代码不是完全的js，因此需了解node编程


express
=======
Routes 
are kind of like a combination of models and controllers in this setup – they direct traffic and also contain some programming logic (you can establish a more traditional MVC architecture with Express if you like. 

app.js
the heart and soul of our app

app.use
用来建立中间件，establishing middleware.



备忘
--------
1. 主模块作为程序入口点，所有模块在执行过程中只初始化一次
2. 有经验的C程序员在编写一个新程序时首先从make文件写起。同样的，使用NodeJS编写程序前，为了有个良好的开端，首先需要准备好代码的目录结构和部署方式，就如同修房子要先搭脚手架。
	- index.js: 入口文件
	- package.json: 自定义入口文件
3. 环境变量就是目录的路径的集合。路径之间在Linux下使用:分隔，用于指定默认的搜索目录
4. $ chmod +x /home/user/bin/node-echo.js 赋予文件执行权限
5. /usr/local/bin  全局可执行的文件
6. 以编写一个命令行程序为例，一般我们会同时提供命令行模式和API模式两种使用方式，并且我们会借助三方包来编写代码