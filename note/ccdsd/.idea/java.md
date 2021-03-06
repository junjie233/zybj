1、什么是JavaScript

JavaScript是一种轻量级的脚本语言。
脚本语言：指的是它不具备开发操作系统的能力，而是只用来编写控制其他大型应用程序的“脚本”。
JavaScript的组成：
ECMAScript:一套标准，最新的标准是ES6（简称）
基本的语法构造：比如操作符、控制结构、语句
标准库：Array、Date、Math等
BOM：Browser Object Model，浏览器对象模型
DOM：Document Object Model，文档对象模型
文档树 DOM 【DOM参考】
2、JavaScript的发展史

JavaScript之父 —— 布兰登·艾奇(Brendan Eich)
1995年网景(Netscape)公司开发，用时10天设计了JavaScript的第一版。
基本语法：借鉴C语言和Java语言。 数据结构：借鉴Java语言，包括将值分成原始值和对象两大类。 函数的用法：借鉴Scheme语言和Awk语言，将函数当作第一等公民，并引入闭包。 原型继承模型：借鉴Self语言（Smalltalk的一种变种）。 正则表达式：借鉴Perl语言。 字符串和数组处理：借鉴Python语言。
1995年12月4日，Netscape公司与Sun公司联合发布了JavaScript语言
1996年3月，Navigator 2.0浏览器正式内置了JavaScript脚本语言。
1997年，以JavaScript1.1为蓝本的建议被提交给了欧洲计算机制造商协会（ECMA）该协会指定39号技术委员会负责将其进行标准化。经过数月的努力完成了ECMA-262——定义了一种名为ECMAScript的新脚本语言的标准。
JavaScript的版本：
1997年7月，ECMAScript 1.0发布。
1998年6月，ECMAScript 2.0版发布。
1999年12月，ECMAScript 3.0版发布，成为JavaScript的通行标准，得到了广泛支持。
2007年10月，ECMAScript 4.0版草案发布，对3.0版做了大幅升级，预计次年8月发布正式版本
2009年12月，ECMAScript 5.0版正式发布。
2011年6月，ECMAscript 5.1版发布，并且成为ISO国际标准。到了2012年底，所有主要浏览器都支持ECMAScript 5.1版的全部功能。
2013年12月，ECMAScript 6草案发布。
2015年6月，ECMAScript 6正式发布。
3、JavaScript的可以干什么？

浏览器的平台化 随着HTML 5的出现，浏览器本身的功能越来越强，不再仅仅能浏览网页，而是越来越像一个平台，JavaScript因此得以调用许多系统功能，比如操作本地文件、操作图片、调用摄像头和麦克风等等。这使得JavaScript可以完成许多以前无法想象的事情。
Node Node项目使得JavaScript可以用于开发服务器端的大型项目，网站的前后端都用JavaScript开发已经成为了现实。有些嵌入式平台（Raspberry Pi）能够安装Node.js，于是JavaScript就能为这些平台开发应用程序。
数据库操作 JavaScript甚至也可以用来操作数据库。NoSQL数据库这个概念，本身就是在JSON（JavaScript Object Notation，JavaScript对象表示法）格式的基础上诞生的，大部分NoSQL数据库允许JavaScript直接操作。基于SQL语言的开源数据库PostgreSQL支持JavaScript作为操作语言，可以部分取代SQL查询语言。
跨移动平台 JavaScript也正在成为手机应用的开发语言。一般来说，安卓平台使用Java语言开发，iOS平台使用Objective-C或Swift语言开发。许多人正在努力，让JavaScript成为各个平台的通用开发语言。 PhoneGap项目就是将JavaScript和HTML5打包在一个容器之中，使得它能同时在iOS和安卓上运行。Facebook的React Native项目则是将JavaScript写的组件，编译成原生组件，从而使它们具备优秀的性能。 Mozilla基金会的手机操作系统Firefox OS，更是直接将JavaScript作为操作系统的平台语言。
嵌脚本语言 越来越多的应用程序，将JavaScript作为内嵌的脚本语言，比如Adobe公司的著名PDF阅读器Acrobat、Linux桌面环境GNOME 3。
跨平台的桌面应用程序 Chromium OS、Windows 8等操作系统直接支持JavaScript编写应用程序。Mozilla的Open Web Apps项目、Google的Chrome App项目、Github的Electron项目、以及TideSDK项目，都可以用来编写运行于Windows、Mac OS和Android等多个桌面平台的程序，不依赖浏览器。