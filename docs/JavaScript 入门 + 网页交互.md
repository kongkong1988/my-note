## JavaScript 简介

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。

### JavaScript 是脚本语言

- JavaScript 是一种轻量级的编程语言.
- JavaScript 是可插入 HTML 页面的编程代码.
- JavaScript 插入 HTML 页面后,可由所有的现代浏览器执行.
- JavaScript 很容易学习.

### JavaScript: 直接吸入 HTML 输出流

	您只能在 HTML 输出中使用 document.write。如果您在文档加载后使用该方法，会覆盖整个文档。

### JavaScript: 对事件的反应

alert() 函数在 JavaScript 中并不常用，但它对于代码测试非常方便。

onclick 事件只是您即将在本教程中学到的众多事件之一。

### JavaScript: 改变 HTML 内容

您会经常看到 document.getElementById("some id")。这个方法是 HTML DOM 中定义的。

DOM (Document Object Model)（文档对象模型）是用于访问 HTML 元素的正式 W3C 标准。

您将在本教程的多个章节中学到有关 HTML DOM 的知识。

### JavaScript: 改变 HTML 图像

### JavaScript: 改变 HTML 样式

改变 HTML 元素的样式,属于改变 HTML 属性的变种.

### JavaScript: 验证输入

JavaScript 常用于验证用户的输入.

## JavaScript 用法

- HTML 中的 Javascript 脚本代码必须位于 <script> 与 </script> 标签之间。

- Javascript 脚本代码可被放置在 HTML 页面的 <body> 和 <head> 部分中。

### <script> 标签

如需在 HTML 页面中插入 JavaScript，请使用 <script> 标签。

<script> 和 </script> 会告诉 JavaScript 在何处开始和结束。

### <body> 中的JavaScript

JavaScript 可在页面加载时想 HTML 的 '<body>' 写文本.

### JavaScript 函数和事件

JavaScript 语句，会在页面加载时执行。

通常，我们需要在某个事件发生时执行代码，比如当用户点击按钮时。

如果我们把 JavaScript 代码放入函数中，就可以在事件发生时调用该函数。

您将在稍后的章节学到更多有关 JavaScript 函数和事件的知识。

### 在 <head> 或者 <body> 的 JavaScript

您可以在 HTML 文档中放入不限数量的脚本。

脚本可位于 HTML 的 <body> 或 <head> 部分中，或者同时存在于两个部分中。

通常的做法是把函数放入 <head> 部分中，或者放在页面底部。这样就可以把它们安置到同一处位置，不会干扰页面的内容。

### <head> 中的 JavaScript 函数

在本例中,我们把一个 JavaScript 函数放置到 HTML 页面的 <head> 部分.

该函数会在点击按钮时被调用:

```
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</head>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
</body>
</html>
```

### <body> 中的 JavaScript 函数

在本例中,我们把一个 JavaScript 函数放置到 HTML 页面的<body> 部分.

该函数会在点击按钮时被调用:

```
<!DOCTYPE html>
<html>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</body>
</html><!DOCTYPE html>
<html>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</body>
</html>
```

### 外部的 JavaScript

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 .js。

如需使用外部文件，请在 <script> 标签的 "src" 属性中设置该 .js 文件：

```
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

你可以将脚本放置于 <head> 或者 <body>中，放在 <script> 标签中的脚本与外部引用的脚本运行效果完全一致。

myScript.js 文件代码如下：

```
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
```

外部脚本不能包含 '<script>' 标签.

## JavaScript Vscode & AI 编程助手

VSCode 完整安装教程参考：https://www.runoob.com/vscode/vscode-tutorial.html

AI 编程助手 —— Fitten Code

## Chrome 浏览器中执行 JavaScript 

参考 https://www.runoob.com/js/js-chrome.html

## JavaScript 输出

### JavaScript 没有任何打印或者输出的函数

### JavaScript 显示数据

JavaScript 可以通过不同的方式来输出数据：

- 使用 window.alert() 弹出警告框.

- 使用 document.write() 方法将内容写到 HTML 文档中。

- 使用 innerHTML 写入到 HTML 元素。

- 使用 console.log() 写入到浏览器的控制台。

### 使用 window.alert()

可以弹出警告框来显示数据:

```
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个页面</h1><p>我的第一个段落。</p>
	
<script>window.alert(5 + 6);
</script>

</body>
</html>
```

### 操作 HTML 元素

如需从 JavaScript 访问某个 HTML 元素,可以是使用 document.getElementByld(Id) 方法.

请使用 'Id' 属性来表示 HTML 元素,bing innerHTML 来获取或插入元素内容:

```
<!DOCTYPE html><html>
<body>

<h1>我的第一个 Web 页面</h1>

	<p id="demo">我的第一个段落</p>

<script>
	document.getElementById("demo").innerHTML = "段落已修改。";
</script>

</body>
</html>
```

以上 JavaScript 语句 (在<script>标签中) 可以在 web 浏览器中执行:

**document.getElementByld("demo")** 是使用 Id 属性来查找 HTML 元素的 JavaScript 代码.

**innerHTML="段落已修改."** 是用于修改元素的 HTML 内容(innerHTML)的 JavaScript 代码.

***在本教程中*** 
- 在大多数情况下,在本教程中,我们将使用上面描述的方法来输出

- 上面的例子直接把 Id="demo" 的 <p> 元素写到 HTML 文档输出中

### 写到 HTML 问到

处于测试目的,可以将 JavaScript 直接写在 HTML 文档中:

```
<!DOCTYPE html><html>
<body><h1>我的第一个 Web 页面</h1>
	<p>我的第一个段落。</p>
	<script>document.write(Date());
</script>

</body>
</html>
```

- 使用 document.write() 可以向文档写入内容.

- 如果在文档已完成加载后执行 document.write,整个 HTML 页面将被覆盖.

```
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个 Web 页面</h1>
<p>我的第一个段落。</p>
<button onclick="myFunction()">点我</button>
<script>
function myFunction() {
   	document.write(Date());
}
</script>
</body>
</html>
```

### 写到控制台

- 如果浏览器支持调试,可以使用 console.log() 方法在浏览器中显示 JavaScript 值.
- 浏览器中使用 F12 来启用调试模式,在调试窗口中点击 "Console" 菜单.

```
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个 Web 页面</h1>
<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>

</body>
</html>
```

***程序中调试是测试,查找及减少 bug(错误)的过程.***

## JavaScript 语法

JavaScript 是一个程序语言.语法规则定义了语言结构.

### JavaScript 语法

- JavaScript 是一个脚本语言

- 它是一个轻量级,但功能强大的编程语言

### JavaScript 字面量

在编程语言中,一般固定值称为字面量,如 3.14

**数字 (Number) 字面量** 可以是整数或者小数,或者是科学计数(e).

**字符串 (String) 字面量** 可以使用单引号或双引号

**表达式字面量** 用于计算

**数组(Array) 字面量** 定义一个数组

**对象(Object) 字面量** 定义一个对象

**函数(Function) 字面量** 定义一个函数

### JavaScript 变量

在编程语言中,变量用于存储数据值

JavaScript 使用关键字 var 来定义变量,使用等号来为变量赋值:

```
var x, lengthx = 5
length = 6
```

变量可以通过变量名访问.在指令式语言中,变量通常是可变的.字面量是一个恒定的值.

变量是一个**名称**.字面量是一个**值**

### JavaScript 操作符

JavaScript 使用 **算数运算符** 来计算值

JavaScript 使用 **赋值运算符** 给变量赋值

JavaScript 语言有多种类型的运算符:

|类型|示例|描述|
|:---:|:---:|:---:|
|赋值,算数和运算符|= + - * /|在 JS 运算符中描述|
|条件,比较及逻辑运算符|== != < >|在 JS 比较运算符中描述|

### JavaScript 语句

在 HTML 中,JavaScript 语句用于向浏览器发出命令.

语句是用分号分隔:

```
x = 5 + 6;
y = x * 10;
```

### JavaScript 关键字

JavaScript 关键字用于识别要执行的操作.

和其他任何编程语言一样,JavaScript 保留了一些关键字为自己所用.

**var** 关键字告诉浏览器创建一个新的变量:

```
var x = 5 + 6;
var y = x * 10;
```

JavaScript 同样保留了一些关键字,这些关键字在当前的语言版本中并没有使用,但在以后 JavaScript 扩展中会用到.

以下是 JavaScript 中最重要的保留关键字 (按字母顺序):

```
abstract	else	instanceof	super
boolean	enum	int	switch
break	export	interface	synchronized
byte	extends	let	this
case	false	long	throw
catch	final	native	throws
char	finally	new	transient
class	float	null	true
const	for	package	try
continue	function	private	typeof
debugger	goto	protected	var
default	if	public	void
delete	implements	return	volatile
do	import	short	while
double	in	static	with
```

### JavaScript 注释

双斜杠 // 后的内容会被浏览器忽略

### JavaScript 数据类型

JavaScript 有多种数据类型: 数字、字符串、数组、对象等等：

```
var length = 16;                                  // Number 通过数字字面量赋值 
var points = x * 10;                              // Number 通过表达式字面量赋值
var lastName = "Johnson";                         // String 通过字符串字面量赋值
var cars = ["Saab", "Volvo", "BMW"];              // Array  通过数组字面量赋值
var person = {firstName:"John", lastName:"Doe"};  // Object 通过对象字面量赋值
```

数据类型的概念

编程语言中,数据类型是一个非常重要的内容.

为了可以操作变量,了解数据类型的概念非常重要.

如果没有使用数据类型,以下实例将无法执行:

```
16 + "Volvo"
```

16 加上 "Volvo" 是如何计算呢? 以上会产生一个错误还是输出以下结果呢？

```
"16Volvo"
```
可以在浏览器尝试执行以上代码查看效果.

### JavaScript 函数

JavaScript 语句可以写在函数内,函数可以重复引用:

**引用一个函数**=调用函数(执行函数内的语句).

```
function myFunction(a, b) {
   	return a * b;         
                     
// 返回 a 乘以 b 的结果
}
```

### JavaScript 字母大小写

JavaScript 对大小写是敏感的.

当编写 JavaScript 语句时,请留意是否关闭大小写切换键.

函数 **getElementByld** 与 **getElementBylD** 是不同的.

同样,变量 **myVariable** 与 **MyVariable** 也是不同的.

### JavaScript 字符集

JavaScript 使用 Unicode 字符集.

Unicode 覆盖了所有的字符,包含标点等字符.

如需进一步了解,请学习 [完整 Unicode 参考手册](https://www.runoob.com/charsets/ref-html-utf8.html)

***JavaScript 中,常见的是驼峰法的命名规则,如 lastName(而不是lastname).***

## JavaScript 语句

JavaScript 语句向浏览器发出的命名.语句的作用是告诉浏览器该做什么.

### JavaScript 语句

JavaScript 语句是发给浏览器的命令.

这些命令的作用是告诉浏览器要做的事情.

下面的 JavaScript 语句向 id="demo" 的 HTML 元素输出文本 "你好 Dolly":

```
document.getElementById("demo").innerHTML = "你好 Dolly";
```

### 分号 ;

分号用于分隔 JavaScript 语句.

通常我们在每条可执行的语句结尾添加分号.

使用分号的另一用处是在一行中编写多条语句.

```
a = 5;
b = 6;
c = a + b;
以上实例也可以这么写:
a = 5; b = 6; c = a + b;
```

***也可能看到不带有分号的案例.在 JavaScript 中,用分号来结束语句是可选的.***

### JavaScript 代码

JavaScript 代码是 JavaScript 语句的序列.

浏览器按照编写顺序依次执行每条语句.

本例向网页输出一个标题和两个段落:

```
document.getElementById("demo").innerHTML="你好 Dolly";
document.getElementById("myDIV").innerHTML="你最近怎么样?";
```

### JavaScript 代码块

JavaScript 可以分批地组合起来.

代码块以左花括号开始,右花括号结束.

代码块的作用是一并地执行语句序列.

本例向网页输出一个标题和两个段落:

```
function myFunction()
{
    document.getElementById("demo").innerHTML="你好Dolly";
    document.getElementById("myDIV").innerHTML="你最近怎么样?";
}
```

### JavaScript 语句标识符

JavaScript 语句通常以一个 **语句标识符** 为开始,并执行该语句.

语句标识符是留着关键字不能作为变量名使用.

下表列出了 JavaScript 语句标识符(关键字):

|语句|描述|
|:---:|:---:|
|break|用于跳出循环.|
|catch|语句块,在 try 语句块执行出错时执行 catch 语句块.|
|continue|跳过循环中的一个迭代|
|do...while|跳过循环中的一个迭代.|
|for|在条件语句为 true 时,可以将代码块执行指定的次数.|
|for...in|用于遍历数组或者对象的属性 (对数组或者对象的属性进行循环操作).|
|function|定义一个函数|
|if...else|用于基于不同的条件来执行不同的动作.|
|return|返回结果,并退出函数|
|switch|用于基于不同的条件来执行不同的动作.|
|throw|抛出 (生成) 错误.|
|try|实现错误处理,与 catch 一同使用.|
|var|声明一个变量.|
|while|当条件语句为 true 时,执行语句块.|

### 空格

JavaScript 会忽略多余的空格.可以向脚本添加空格,来提高其可读性.下面的两行代码是等效的:

```
var person="runoob";
var person = "runoob";
```

### 对代码行进行折行

可以在文本字符串中使用反斜杠对代码行进行换行.下面的例子是正确的显示:

```
document.write("你好 \
世界!");
```

不过,不能向这样换行:

```
document.write \ 
("你好世界!");
```

**知识点**: JavaScript 是脚本语言,浏览器会在读取代码时,逐行地执行脚本代码.而对于传统编程来说,会在执行前对所有代码进行编译.

## JavaScript 注释
