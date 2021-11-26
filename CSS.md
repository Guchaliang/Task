# CSS



## 1.颜色关键词

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



## 2.字体

**font-family:Arial, Helvetica, sans-serif;**

*三者都是字体族名*

sans-serif与serif的区别就是有衬线与无衬线

==在使用的时候需要注意空格时要加上双引号==

monospace是等宽字体

需要考虑到使用的字体是否被电脑支持



font-weight  (字重)

font-style (字体)

text-transform(大小写)

letter-spacing(字母间距)

word-spacing(单词间距)



## 3.盒子模型(箱模型)【border】

外边距塌陷：当两个盒子合在一起时只有一个外边距(且是最大的外边距)

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

---

p {	

​	margin:5px 10px;(上下边距相同，左右边距相同)

}

---

p {

​	margin: 5px 10px 5px;(上边距，左右边距相等，下边距)

}



==三块内容放在一起需要使用float==

需要注意的是边框也会占宽度

注意需要将浮动清除掉

