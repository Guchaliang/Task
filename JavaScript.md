# JavaScript



JavaScript不区分整数型和浮点型



## 1.变量

**定义变量使用==var==(全局变量)以及==let==（局部变量)**

例如：var name     let=a

尽量常用let



**输出使用console.log()**



const 仍然是常量，但是使用是就直接**const PI**



==注意==：x="3"+4+5  与 x="3"+"4"+"5"等价

但是  x=3+4+"5" 与  x="3"+4+5并不等价，它与

x=7+"5"等价



## 2.控制结构

基本与C语言相同

可以在赋值的时候就进行一些特殊操作

如:var allowed = ( age >= 18) ? "yes" : "no"





## 3.对象

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



## 4.数组

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





## 5.函数

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



## 6.闭包(常用)

function makeAdder (a) {

​	return function (b) {

​	return a+b;

​	};

}



var x = makeAdder(5);

var sum = x(6); 





## 注意：

== 与 ===是不同的；

==可以进行字符转换

===不进行字符转换