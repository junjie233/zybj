## 
1.什么是JAVAScript
 JAVAScript是一种轻量级的脚本语言
 脚本语言：指的是它不具备开发操作系统的能力，而是只用来编写控制其他大型应用程序的“脚本”。

### 组成
JavaScript的组成：

ECMAScript:一套标准，最新的标准是ES6（简称）
基本的语法构造：比如操作符、控制结构、语句
标准库：Array、Date、Math等
BOM：Browser Object Model，浏览器对象模型
DOM：Document Object Model，文档对象模型

### 发展历史
1997年，以JavaScript1.1为蓝本的建议被提交给了欧洲计算机制造商协会（ECMA）该协会指定39号技术委员会负责将其进行标准化。经过数月的努力完成了ECMA-262——定义了一种名为ECMAScrip（最出名的是ECMAScrip）的新脚本语言的标准
2015年之前用的最多的是ECMAScript 5.0
2015年6月，ECMAScript 6正式发布

### JS 的应用
+ 网页
 焦点图/幻灯片  tab切换 动画 拖拽 像素
 + node
   服务器端
 + 数据库
+ 跨平台 （react native， cordova， apicloud ，webapp（jquery mobile， weui，mui， muf， angular，bootstrap）
+ 桌面程序

 数据库关系划分
 + 关系型数据库（oracle， mysql..）
 + 非关系型数据库（NosqL）
    + mongobd
    + postgresql

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>

    </style>
</head>
<body>
    <!--css放在head里面
    js文件在</body>之上插入
    -->
    
<script>
    alert("sde");//弹出对话框//
    document.write("cadsaasd");
    console.log("cdaas");//插入对话框答案输入区域//
    prompt("需要什么");//插入对话框问题//
</script>
</html>
```




# h1 

## h2

### h3

### h6

```
正文
```
+ 无序列表
+ 无序列表
+ 无序列表
+ 无序列表
> 标注，引用

正文相隔两行才换行


正文相隔两行才换行

# 列表

## 插入图片
! [we]()

## 超链接
[简书]()

## 怎么将md文件转换成pdf文件

+ 收索pdf安装
+ 重新打开页面
+ ctrl+shift+p 或者 F1 收索pdf 回车


# 变量
+ 概念：可以存储数据的一个容器。可以存储和引用任何的数据
+ 声明（var:所有浏览器都支持 ，let：有局限性不是所有都支持但用它比较好）
+ 作用域（于函数章节具体说明）
    + 全局变量
    + 局部变量

# 标识符
+ 必须以字母，下划线或者$开头
+ 余下的部分可以是任意的字母，数字，下划线或$
+ 不能用关键字，或者是保留字名字
+ 变量区分大小写
+ 命名需见名知意
+ 大多采用驼峰命名法：var abook="", var ABook=""