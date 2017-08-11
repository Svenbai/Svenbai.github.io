#JavaScript 数据类型
***
###字符串、数字、布尔、数组、对象、Null、Undefined
***

* #####null：空、无。表示不存在，当为对象的属性赋值为null，表示删除该属性
* #####undefined：未定义。当声明变量却没有赋值时会显示该值。可以为变量赋值为undefined
* #####number：数值。最原始的数据类型，表达式计算的载体
* #####string：字符串。最抽象的数据类型，信息传播的载体
* #####boolean：布尔值。最机械的数据类型，逻辑运算的载体
* #####object：对象。面向对象的基础
**** 
	alert(typeof 1);      		 	 // 返回字符串"number"
	
    alert(typeof "1");            	  // 返回字符串"string"  
    
    alert(typeof true);           	  // 返回字符串"boolean" 
     
    alert(typeof {});            	   // 返回字符串"object"  
    
    alert(typeof []);              	 // 返回字符串"object "  
    
    alert(typeof function(){});   	  // 返回字符串"function"  
    
    alert(typeof null);             // 返回字符串"object"  
    
	alert(typeof undefined);        // 返回字符串"undefine"
###需要注意的:	
1.`	typeof NaN === 'number';`

2.`typeof undefined === 'undefined';`

3.`typeof [1, 2, 4] === 'object';`

4.`typeof new Date() === 'object';`

5.`typeof null === 'object';`

6.`typeof function(){} === 'function';`

***
#变量
***
####变量是用来保存存储内容的空间

####js变量只能用var关键字定义
	var x=2;
	var y=3;
	var z=x+y;在代数中，我们使用字母（比如 x）来保存值（比如 2）。
通过上面的表达式 z=x+y，我们能够计算出 z 的值为 5。
在 JavaScript 中，这些字母被称为变量。
`提示：可以把变量看做存储数据的容器。`####一条语句，多个变量
可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可：

	var name="Gates", age=56, job="CEO";
	
###一、变量提升
	console.log(global);        // undefined
	var global = 'global';
	console.log(global);        // global
	function fn () {
	console.log(a);            // undefined
	var a = 'aaa';
	console.log(a);           // aaa
	  }
	fn();
之所以会是以上的打印结果，是由于js的变量提升，实际上上面的代码是按照以下来执行的：

	var global;                // 变量提升，全局作用域范围内，此时只是声明，并没有赋值
	console.log(global);        // undefined
	global = 'global';          // 此时才赋值
	console.log(global);       // 打印出global
	function fn () {
	var a;                    // 变量提升，函数作用域范围内
	console.log(a);
	a = 'aaa';
	console.log(a);
	}
	fn();

