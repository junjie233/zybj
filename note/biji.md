```
#清除浮动
浮动带来的影响
加浮动元素的父级会没有高度
加浮动元素的后面的布局会受到影响

##第一种方式
html
```css
<div class="par">
<div></div>
<div></div>
<p class="clear"></p>
</div>
```

css
```css
.par div{
    width: 200px;
    height: 200px;
    background-color: #908;
    float: left;
}
/*清除浮动*/
.clear{
    clear；both;
}
```

这种方式的问题：

+ 每次使用时还需另外加上一个盒子

## 第二种方式
html
```html
<div class="par">
    <div></div>
    <div></div>
</div>
```

css
```css
.clear{
    zoom:1;/*为了兼容IE7**/
}
.clear::after{      /**after:。。。之后**/
            content: "";
            display: block;
            clear: both; /**清除浮动**/
        }
```
# css伪对象
+ `::after`:对象之后发生的内容
+ `::before`:对象之后发生的内容
 他们常跟`content`连用，content是必须的。
 html
 
 ```html
<div class="par clear"></div>
css
 .clear::after{
     content:""
 }
```
# 注释

对我们的代码进行解释，不会在程序中运行

## html中的注释
```html
<!--注释内容-->

```
`vscold`中的快捷方式`ctrl+/`

## css中的注释

```css
/*注释内容*/
```
快捷键`ctrl+/`


#边框

##复合样式

```css
    border:1px solid #000;

```

# html中插入css样式的方式

+ 外部样式
+ 内部样式
+ 行内样式

## 内嵌样式

```html

 <style>
    /*具体的样式*/
 
 </style>

```
>使用该方式时，建议将`style`标签写到head中间。

## 内联样式/行内样式

```css
<div style="background: #f00; font-size:100px; "></div>
```

# 盒子模型

+ margin
+ border
+ padding

## margin`padding的参数

+ 一个参数（`margin:10px`）:上右下左都为10像素
+ 两个参数：(`margin:10px 20px`)上下为10，左右为20
+ 三个参数(`margin:5px 10px 20px`):上为5px，左右为10px，下为20px
+ 四个参素（`margin:5px 10px 20px 25px`）:上为5，右为10，下为20，左为25
 
>padding的参数设置和margin一样

margin和padding还可以分开写：

+ margin-top:上边距
+ margin-right:右边距
+ margin-bottom:下边距
+ margin-left:左边距

> padding同样可以使用top，right，bottom，left来分开写



## margin和padding的区别

+ 盒子设置padding后，宽高会发生响应的变化
+ 设置margin，只会增加距离，而不会改变盒子本身的大小

## border

+ border设


# box-sizing

+ content-box（默认）:padding、border**不被包含**在width和height中
+ border-box:padding、border**包含**在width和height中
 
 html
```html
    <div></div>
 
```

css
```css
div{
    width:100px;
    height:100px;
    padding:10px;
    border:1px solid #000;
}

```

如果在**div**中设置`box-sizing: border-box`，那么div的宽高都不会变化依旧为**100px*100px**，反之将div设置为`box-sizing: content-box`，那么div烦人宽高为**122px*122px**

## 

html
```html
<div class="k">
    <div>
    </div>
</div>
```

css
```css
.k{
    width: 100px;
    height: 100px;
}
.k div{
     padding: 10px;;
}


# display

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: #908;
            display: inline;/*设置宽高无效*/
            display:block;/*有效*/
            display: none;
           /*block: 设置成块级元素；将设置display:none的元素显示
             none：将元素隐藏
             inline-block；行内块级元素，可以设置宽高，不会占一整行
             inline:设置成行内元素、不能设置宽高，不占一整行，只会占文字大小
           */
        }
    </style>
    
</head>```


## 块级元素
+ h1-h6
+ p
+ ul
+ ol
+ li
+ div
## 行内元素
+ span
+ a
+ img
 
## 行内块级元素


##块级元素转换成行内元素
html
```html
<div>df</div>

```
css
```css
{width:20px;
 height：20px;
 display:inline;

}

```



## 行内元素转换成行内块级元素

html
```html
<span>sd</span>

```

css
```css
span{
            width:20px;
            height：20px;
            display:block;

        }

```

## 块级元素转换成**行内块级**元素

html
```html
<div>df</div>

```
css
```css
span{
      width:20px;
      height：20px;
      display:inline-block;

}
```

# 背景

+ background：复合属性；
+ background-color：背景颜色   #000
+ background-image：背景图片     url()
+ background-position：背景图片的位置    0  0(相当于一个坐标)
+ background-repeat：背景是否重复     no-repeat

## background-image（背景图片）
```css


```

##  background-repeat（背景图片是否重复）
+  repeat:水平垂直方向都重复
+  repeat-x：水平方向重复
+  repeat-y：垂直方向重复
+  no-repeat：不重复


## background（复合属性）





# 选择符

+ 元素
+ 关系
+ 属性
+ 伪类
+ 伪对象

## 元素选择符（器）

+ “*”，通配符，选择的是所有html标签
+ “E”，标签选择器，选择的标签如，`p{}`,`li{}`
+ "E#ids",id选择器，选择元素E设置了id的值为ids的元素，如`div#head`
+ "E.class",类选择器，选择元素E设置了class的值为class的元素，如:`div.head`

## 关系选择符

+ `E F`:包含选择符，选择的E下的所有的F元素，如：`ul li`,`.menu li`
+ `E>F`:子选择器，选择E下复合条件F的所有子元素，如：`.menu>li`
+ `E+F`:兄弟选择器，选择的是E之后的第一个元素，E和F必须是同级，如：`.nav+p`
`E~F`:选择E只有所有F元素，如：`nav~p`

## 属性

+ E[att]:选择E元素包含属性att的所有标签，如：`div["class"]`
+ E[att="val"]:选择E元素中属值为vl的标签，如：`div[class="head"]`

## 伪类
+ E：hover：鼠标移上去的样式
+ E:nth-child（n）：选择第n个元素，常见有2n，2n-1 ......
+ E：first-child：选择第一个元素，如：`li:first-child{}`
+ E：last-child：选择最后一个元素，如：`li:last-child{}`

## 伪对象
+ E：after/E：：after  ：在内容之后发生的内容`.clear:after{}`
+ E：before/E：：before  ：在内容发生之前发生的内容，如：`.a:before{}`
+ 一般和content连用





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
   
    <title>表单t</title>
</head>
<body>
    <!--
        action:表单数据提交到哪
        methon：指用什么方法提交数据，get，post

        get与post提交数据的区别：
        + get传输数据大小有限，不安全（在浏览器地址栏可以看到提交的数据）
        + post 方式传输数据相对较大，比get方式安全

        http/https 协议（请求头，请求的内容）
    -->
    <form action="">
    <!-- text:文本输入框-->
    <input type="text" name="" id="">
    </form>
</html>









<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <title>表单t</title>
</head>
<body>
<!--
    action:表单数据提交到哪
    methon：指用什么方法提交数据，get，post

    get与post提交数据的区别：
    + get传输数据大小有限，不安全（在浏览器地址栏可以看到提交的数据）：一般用于获取数据
    + post 方式传输数据相对较大，比get方式安全：一般用于提交数据

    http/https 协议（请求头，请求的内容）
-->
<form action="" method="get">
    <!-- text:文本输入框-->
    <!--label:标签 -->
    <!--
    type:输入框的类型
    name：这个输入框的名字，一般一个name值在一个form中不能重复，checkbox除外
    id：给input起一个唯一名字
    value:默认的值
    checkbox: 复选项（多选项），name值为：“名字[]"
    radio：单选框，需要写入value的值，单选框组合的name的值必须一致
    button：普通按钮
    reset:重置按钮
    -->
    <label for="username">用户名：<input type="text" name="user" id="username" value="3434">
        <br />

       <label for="passwod"> 密码：<input type="password" name="pwd" id="passwod">
            <br />
            <label for="sex"> 性别：</label>
            <!--checked:表示默认选中-->
            <input type="radio" name="sex" value="man" id="sex"/>男
            <input type="radio" name="sex" value="woman" id="sex" checked="checked"/>女
            <br />
            <input type="checkbox" name="[]" id="" value="1">篮球
            <input type="checkbox" name="[]" id="" value="2">足球
            <input type="checkbox" name="[]" id="" value="3">羽毛球
            <br />
            <input type="submit" value="提交">
            <input type="submit" value="普通按钮">
            <button>普通按钮</button>
            <input type="reset" value="重置">
    </form>

        <!--
        cursor:poiner 鼠标放上去变手
        hover 颜色改变
        -->

</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

</head>
<body>
<form action="">
    <!--
    限制条件
    + readonly：只读
    + required：必填选项
    + pattern:正则验证
    + maxlength：最大长度
    + disabled:禁用
    -->
    <input type="text" name="" value="甲亢" id="" readonly>
    <br>
    <input type="password" name="" value="甲亢" id="">
    <br>
    <input type="text" maxlength="11" pattern="[0-9]{11}">
    <input type="number" max="10" min="5" step="2">
    <input type="range" max="100" min="0" step="10" value="0">
    <input type="submit"  value="提交" >
    <div class="text"></div>
</form>

</body>
</html>
