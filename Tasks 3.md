# 1.HTML(最基础的内容)

### 1.基础模块

基础模块是每个HTML文件必备的

<!DOCTYPE html>    ==解释文档的类型==*解释这是一个HTML文档*

<html>    **==开始标签==**

​    <head>  ==网页名== ~与网页内容无关~

​    </head>

​    <body> ==网页内容==



​    </body>

</html>  ==**结束标签**==



### 2.标签

- <h1>，<h2>和makerdown的一级标题二级标题有点像

- <p>的实际意义是展示，类似于写一个段落

- <strong>为加粗文字

- <em>为斜体

- 超链接<a>，跳转到某一个网站一般使用<a href="网址">单引号与双引号都可以。

  ​    一般来讲，不会让网站跳转到其他网站，而是另外再打开一个网站。

  ​    对比：<a href="https://www.bilibili.com/">

  ​

  <a href="https://www.bilibili.com/" target="_blank">

- <ul>是无序标题，<ol>是有序标题

- 表格 需要将所有的内容放在<table>里

  - <thead>  table head 表头


  - <tr>(不能单独使用,必须放在<table>里)定义一行标签，一组行标签内可以建立多组由<td>或<th>标签所定义的单元格
  - <th>定义表头单元格。表格中的文字将以粗体显示.
  - <td>定义单元格标签，一组<td>标签将将建立一个单元格

- 表单<form>，这个需要注意的是一般使用<form action="form.js"(去数据库form.js寻找) method="POST"而后面的 method应该是查找路径之类的

- 按钮<button>

- 图片<img>,一般使用<img  src=" "  alt=" ">

  - <img>代表图片，这个可以是本地图片也可以是网络图片 
  - src=""写地址 alt=""是当某些原因未显示图片时，显示这句话

- 引用 <abbr>以及<cite>

[更多的需要去网址查找]((https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element)



### 3.属性

[属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Attributes)

[全局属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes)

[更多](https://developer.mozilla.org/zh-CN/docs/Web/HTML)







# 2.CSS(对HTML的布局交互进行处理)

个人感觉CSS更偏向于应用，但是仍有特殊的地方

### 1.添加CSS的三种方式

- 外部样式表

  - CSS保存在.css文件中
  - 在 HTML 文件中使用 <link> 引用

- 内部样式表

  - 不使用外部CSS文件
  - 将 CSS 放在 HTML <style> 里

- 内联样式

  - 仅仅影响一个元素
  - 在HTML 元素的style属性中添加

  ​

  这三种里只推荐使用**==外部样式表==**与**==内部样式表==**

  ​

### 2.Class 与 ID

- Class
  - 注意使用的时候可以使用  .class  快速打出来
  - 这个是可以重复的
- ID
  - 注意使用的时候可以使用  #id  快速打出来
  - 这个在HTML文件中是唯一的，也就是不能有重复的



### 3.颜色关键词

- 关键词

  black ,silver ,white


- 十六进制值

  #ff0000


- RGB(红黄蓝)

  rgb(255,0,0)


- HSL(色相 饱和度 亮度)

  hsl(0,100%,50%)


- RGBA

​       rgb(255,0,0,==0.5==) 【注意这个数取值在0~1之间,0代表完全透明,1代表完全不透明】



- HSlA

  hsl(0,100%,50%,0.5)

  ​

  ### HSL(色相 饱和度 亮(明)度)

  ​

==注意== 任何颜色饱和度为0时就显示灰色，100%时就是全彩；任何颜色亮度0时是黑色，100%时是白色.



### 4.字体【font】

**font-family:Arial, Helvetica, sans-serif;**

*三者都是字体族名*

sans-serif与serif的区别就是有衬线与无衬线

==在使用的时候需要注意空格时要加上双引号==

monospace是等宽字体

需要考虑到使用的字体是否被电脑支持



- font-weight  (字重)


- font-style (字体)
- text-transform(大小写)
- letter-spacing(字母间距)


- word-spacing(单词间距)

也可以直接使用 font



### 5.盒子模型(框模型)

- 边框<border>这个平时是不展示的，但是可以指定颜色让他显示

  - 需要注意的是边框也会占宽度、

    ==使用box-sizing:border-box解决==

  - border：

  - border-right:

  - border-left:

  - border-top:

  - border-bottom:

    ​

  - border-bottom-width:

  - border-bottom-style:



- 内边框<padding>即内容和 <border>之间的距离
  - padding-top:
  - padding-bottom:
  - padding-left:
  - padding-right:



- 外边框<margin>

  - 与上同

  ​

==**外边距塌陷(外边距重叠)**==：当两个盒子合在一起时只有一个外边距(且是最大的外边距)

p {

​	margin-top=5px;

​	margin-bottom=5px;

​	margin-right=10px;

​	margin-left=10px;

}

这个CSS与下面这些形式是相同的



p {

​	margin: 5px 10px 5px 10px;(上，右，下，左)

}

------

p {	

​	margin:5px 10px;(上下边距相同，左右边距相同)

}

------

p {

​	margin: 5px 10px 5px;(上边距，左右边距相等，下边距)

}





### 6.按钮【button】

- 与其他的差不多
- ==状态==
  - ==这个总是忘记==；使用button:启用状态
- 固定按钮（见下方的fixed)





### 7.浮动【float】

- <float>
  - 多用于几个内容需要并排使用的时候
  - 注意这个时候需要清除浮动

**<div class="clearfix">**

**.clearfix {**

  **clear: both;**

**}**

否则会使影响布局



### 8.选择器

[选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors)





### 9.定位【position】（偏移）

- static  --静态定位    所以语言书默认的定位
- relative  --相对定位   与static相似
  - 也就是其原有空间能够保留，也就是可以出现空间的变化
- absolu  --绝对定位 
  - 其会将空间一起偏移
- fixed  --固定定位
  - ​
- sticky



### 10.[更多](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)



# 3.JavaScript（这个用的太少了）

JavaScript不区分整数型和浮点型



### 1.变量

**定义变量使用==var==(全局变量)以及==let==（局部变量)**

例如：var name     let=a

尽量常用let



**输出使用console.log()**



const 仍然是常量，但是使用是就直接**const PI**



==注意==：x="3"+4+5  与 x="3"+"4"+"5"等价

但是  x=3+4+"5" 与  x="3"+4+5并不等价，它与

x=7+"5"等价



### 2.控制结构

基本与C语言相同

可以在赋值的时候就进行一些特殊操作

如:var allowed = ( age >= 18) ? "yes" : "no"





### 3.对象

两种定义方式：

var obj = new object{}；

var obj = {};



obj={

​	name:

​	tel:

​	email:

​	contact:{

​		phone:

​		age:

​	}

}





### 4.数组

var a = new Array();

var b = [];

其余与C语言差不多

输出可以不用写后面的编号，但具体输出要写



==for in==：用于输出全部的值

for ( let i in a){

​	console.log ( a[i] );

}



b. ==push== ("sheep") 这个可以在末尾追加一个sheep

b. ==pop==()  从末尾删除一个值

b. ==shift==()  从开头删除第一个值

b. ==unshift==("")  在开头添加一个引号里的值

b.==reverse==() 倒置数组





### 5.函数

使用==function==添加函数；
传入形参时不要用var啥的；

后面与C语言相同；



不同：function add( ) {

​	let sum = 0;

​	for (let i = 0 , j = ==arguments==.length ; i<j ; i ++){

​	sum += ==arguments== [i];

​	}

​	return sum;

}

此时这个add的括号里可以添加n个值





### 6.闭包(常用)

function makeAdder (a) {

​	return function (b) {

​	return a+b;

​	};

}



var x = makeAdder(5);

var sum = x(6); 



### 注意：

== 与 ===是不同的；

==可以进行字符转换

===不进行字符转换







# 4.最近学习情况

- JavaScript 刚学不久，但是我感觉我用的很少？
  虽然学的时候UP主说的是很常用，JavaScript可以可以调控HTML和CSS是如何实现的?

  ​

  ​

- 关于CSS中的盒子模型，这个水平居中大概知道了

  但是上下居中呢？我自己写的demo是使用margin-top