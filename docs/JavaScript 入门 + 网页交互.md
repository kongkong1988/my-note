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

JavaScript 注释可用于提高代码的可读性.

### JavaScript 注释

JavaScript 不会执行注释.

可以添加注释来对 JavaScript 进行解释,或者提高代码的可读性.

单行注释以 // 开头.

本例用单行注释来解释代码:

```
// 输出标题：
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
// 输出段落：
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```

### JavaScript 多行注释

多行注释以 /* 开始,以 */ 结尾.

下面的例子使用多行注释来解释代码:

```
/*
下面的这些代码会输出
一个标题和一个段落
并将代表主页的开始
*/
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```

### 使用注释来阻止执行

在下面的例子中,注释用于阻止其中一条代码行的执行 (可用于调试):

```
// document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```

在下面的例子中,注释用于阻止代码块的执行 (可用于调试):

```
/*
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
*/
```

### 在行末使用注释

在下面的例子中,我们把注释放到代码行的结尾处:

```
var x=5;    // 声明 x 并把 5 赋值给它
var y=x+2;  // 声明 y 并把 x+2 赋值给它
```

## JavaScript 变量

变量是用于存储信息的"容器".

在 JavaScript 中,变量用于存储数据,并可以在程序执行过程中动态更改.

在 JavaScript 中,变量可以存储各种类型的数据,如数字、字符串、对象、函数等.

变量名是标识符,用于引用存储在变量中的数据.

在 JavaScript 中,可以使用 var、let 和 const 关键字来声明变量。

- var：ES5 引入的变量声明方式，具有函数作用域。

- let：ES6 引入的变量声明方式，具有块级作用域。

- const：ES6 引入的常量声明方式，具有块级作用域，且值不可变。

```
var x=5;
var y=6;
var z=x+y;
```

**就像代数那样**

x=5

y=6 

z=x+y

在代数中,我们使用字母(比如 x) 来保存值 (比如 5).

通过上面的表达式 z=x+y,我们能够计算出 z 的值为 11.

在 JavaScript 中,这些字母被称为变量.

***可以把变量看作存储数据的容器.***

### JavaScript 变量

与代数一样,JavaScript 变量可用于存放值 (比如 x = 5) 和表达式 (比如 z = x + y).

变量可以使用短名称 (比如 x 和 y),也可以使用描述性更好的名称 (比如 age,sum,totavolume).

- 变量必须以字母开头

- 变量也能以 $ 和 _ 符号开头 (不过我们不推荐这么做)

- 变量名称对大小写敏感 (y 和 Y 是不同的变量)

***JavaScript 语句和 JavaScript 变量都对大小写敏感.***

### JavaScript 数据类型

JavaScript 变量还能保存其他数据类型,比如文本值(name="Bill Gates").

在 JavaScript 中,类似 "Bill Gates" 这样一条文本被称为字符串.

JavaScript 变量有很多种类型,但是现在,我们只关注数字和字符串.

当我们向变量分配文本值时,应该用双引号或单引号包围这个值.

当我们向变量赋的值是数值时,不要使用引号.如果我们用引号包围数值,该值会被作为文本来处理.

```
var pi=3.14;  
// 如果你熟悉 ES6，pi 可以使用 const 关键字，表示一个常量
// const pi = 3.14;
var person="John Doe";
var answer='Yes I am!';
```

### 声明 (创建) JavaScript 变量

在 JavaScript 中创建变量通常称为"声明"变量.

我们使用 var 关键词来声明变量:

```
var carname;
```

变量声明之后,该变量是空的 (它没有值).

如需向变量赋值,请使用等号:

```
carname="Volvo";
```

不过也可以在声明变量时对其赋值:

```
var carname="Volvo";
```

在下面的例子中,我们创建了名为 carname 的变量,并向其赋值"Volvo",然后把它放入 id="demo" 的 HTML 段落中:

```
var carname="Volvo";
document.getElementById("demo").innerHTML=carname;
```

**var 声明特点**:

- 变量可以重复声明 (覆盖原变量).

- 变量未赋值时,默认值为 undefined.

- var 声明的变量会提升 (Hoisting),但不会初始化.

***一个好的编程习惯,在代码开始处,统一对需要的变量进行声明.***

### 一条语句,多个变量

我们可以在一条语句中声明很多变量.该语句以 var 开头,并使用逗号分隔变量即可:

```
var lastname="Doe", age=30, job="carpenter";
```

声明也可横跨多行:

```
var lastname="Doe",
age=30,
job="carpenter";
```

一条语句中声明的多个变量不可以同时赋同一个值:

```
var x, y, z = 1;
```

x,y 为 undefined, z 为 1.

### Value = undefined

在计算机程序中,经常会声明无值的变量.未使用值来声明的变量,其值实际上是 undefined.

在执行过以下语句后,变量 carname 的值将是 undefined:

```
var carname;
```
### 重新声明 JavaScript 变量

若果重新声明 JavaScript 变量,该变量的值不会丢失.

在以下两条语句执行后,变量 carname 的值依然是 "Volvo":

```
var
carname="Volvo"; 
var carname;
```

### JavaScript 算数

我们可以通过 JavaScript 变量来做算数,使用的是 = 和 + 这类运算符:

```
y=5;
x=y+2;
```

### 使用 let 和 const (ES6)

在 2015 年以前,我们使用 var 关键字来声明 JavaScript 变量.

在 2015 后的 JavaScript 版本 (ES6) 允许我们使用 const 关键字来定义一个变量,使用 let 关键字定义的限定范围内作用域的变量.

**let**

let 是 ES6 引入的新变量声明方式,推荐使用.

**let 语法:**

```
let variableName = value;let variableName = value;
```

```
let city = "北京";
let age = 30;
console.log(city, age); // 输出: 北京 30
```

**const**

const 用于定义常量,即一旦赋值后,变量的值不能再被修改.

**const 语法**:

```
const variableName = value;
```

```
const z = 10;
// z = 20; // 报错，常量不可重新赋值
if (true) {
    const z = 20; // 不同的常量
    console.log(z); // 输出 20
}
console.log(z); // 输出 10
```

更多 const 和 let 内容可以参阅: [JavaScript let 和 const](https://www.runoob.com/js/js-let-const.html).

## JavaScript 数据类型

**值类型(基本类型):** 字符串 (String)、数字（Number）、空（Null）、未定义 （undefined）、Symbol。

**引用数据类型:** 对象 （Object）、数组 （Array）、函数 （Function），还有两个特殊的对象：正则 （RegExp） 和 日期 （Date）。

**注:** ***Symbol 是 ES6 引入的一种新的原始数据类型,表示独一无二的值.***

### JavaScript 拥有动态类型

JavaScript 拥有动态类型.这意味着相同的变量可用作不同的类型:

```
var x;               
	// x 为 undefinedvar x = 5;           
	// 现在 x 为数字
var x = "John";      // 现在 x 为字符串
```

变量的数据类型可以使用 typeof 操作符来查看:

```
typeof "John"                // 返回 string
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
```

**typeof[1,2,3,4] 返回 "object"**,这是 JavaScript 早期设计的一个"缺陷",数组本质上是特殊类型的对象.

正确检测数组的方法:

```
Array.isArray([1,2,3]); // true
[1,2,3] instanceof Array; // true
```

### JavaScript 字符串

字符串是存储字符 (比如 "Bill Gates") 的变量.

字符串可以是引号中的任意文本.可以使用单引号或双引号:

```
var
carname="Volvo XC60";
var
carname='Volvo XC60';
```

可以在字符串中使用引号,只要不匹配包围字符串的引号即可:

```
var answer="It's alright";
var answer="He is called 'Johnny'";
var answer='He is called "Johnny"';
```

### JavaScript 数字

JavaScript 只有一种数字类型.数字可以带小数点,也可以不带:

```
var x1=34.00;      //使用小数点来写
var
x2=34;             //不使用小数点来写
```

极大或极小的数字可以通过科学 (指数) 计数法来书写:

```
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```

### JavaScript 布尔

布尔 (逻辑) 只能有两个值:true 或 false.

```
var x=true;
var y=false;
```

### JavaScript 数组

下面的代码创建名为 cars 的数组:

```
var cars=new Array();
cars[0]="Saab";
cars[1]="Volvo";
cars[2]="BMW";
```

或者 (condensed array):

```
var cars=new Array("Saab","Volvo","BMW");
```

或者 (literal array):

```
var cars=["Saab","Volvo","BMW"];
```

### JavaScript 对象

对象由花括号分隔,在括号内部,对象的属性以名称和值对的形式 (name : value) 来定义.属性由逗号分隔:

```
var person={firstname:"John", lastname:"Doe", id:5566};
```

上面例子中的对象 (person) 有三个属性: firstname、lastname 以及 id.

空格和折行无关紧要.声明可横跨多行:

```
var person={
firstname : "John",
lastname  : "Doe",
id        :  5566
};
```

对象属性由两种寻址方式:

```
name=person.lastname;
name=person["lastname"];
```

### Undefined 和 Null

Undefined 这个值表示变量不含有值.

可以通过变量的值设置为 null 来清空变量.

```
cars=null;
person=null;
```

### 声明变量类型

当我们声明新变量时,可以使用关键字 "new" 来声明其类型:

```
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

***JavaScript 变量均为对象.当我们声明一个变量时,就创建了一个新的对象.***

## JavaScript 对象

JavaScript 对象是拥有属性和方法的数据.

在 JavaScript 中,几乎所有的事物都是对象.

***在 JavaScript 中,对象是非常重要的,当我们理解了对象,就可以了解 JavaScript.***

以下代码为变量 **car** 设置值为 "Fiat":

```
var car = "Fiat";
```

对象也是一个变量,但对象可以包含多个值 (多个变量),每个值以 **name:value** 对呈现.

```
var car = {name:"Fiat", model:500, color:"white"};
```

以上实例中,3个值 ("Fiat",500,"white")赋予变量 car.

***JavaScript 对象是变量的容器.***

### 对象定义

你可以使用字符来定义和创建 JavaScript 对象:

```
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

定义 JavaScript 对象可以跨越多行,空格跟换行不是必须的:

```
var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};
```

### 对象属性

可以说 "JavaScript 对象是变量的容器".

但是,我们通常认为 "JavaScript 对象是键值对的容器".

键值对通常写法为 **name : value** (键与值以冒号分隔).

键值对在 JavaScript 对象通常称为 **对象属性**.

***JavaScript 对象是属性变量的容器.***

对象键值对的写法类似于:

- PHP 这种的关联数组

- Python 中的字典

- C 语言中的哈希表

- Java 中的哈希映射

- Ruby 和 Perl 中的哈希表

### 访问对象属性

我们可以通过两种方式访问对象属性:

```
person.lastName;
```

```
person["lastName"];
```

### 对象方法

对象的方法定义了一个函数,并作为对象的属性存储.

对象方法通过添加 () 调用 (作为一个函数).

该实例访问了 person 对象的 fullName() 方法:

```
name = person.fullName();
```

如果要访问 person 对象的 fullName 属性,它将作为一个定义函数的字符串返回:

```
name = person.fullName;
```

***JavaScript 对象是属性和方法的容器.***

### 访问对象的方法

可以使用以下语法创建对象方法:

```
methodName : function() {
    // 代码 
}
```

可以使用以下语法访问对象方法:

```
objectName.methodName()
```

通常 fullName() 是作为 person 对象的一个方法,fullName 是作为一个属性.

如果使用 fullName 属性,不添加 **()**,它会返回函数的定义:

```
objectName.methodName
```

有多种方式可以创建,使用和修改 JavaScript 对象.

同样也有多种方式用来创建,使用和修改属性和方法.

### 更多实例

[创建 JavaScript 对象Ⅰ](https://www.runoob.com/try/tryit.php?filename=tryjs_object_create_1)

[创建 JavaScript 对象 Ⅱ](https://www.runoob.com/try/tryit.php?filename=tryjs_object_create_2)

[访问对象属性Ⅰ](https://www.runoob.com/try/tryit.php?filename=tryjs_object_properties_1)

[访问对象 Ⅱ](https://www.runoob.com/try/tryit.php?filename=tryjs_object_properties_2)

[函数属性作为一个方法访问](https://www.runoob.com/try/tryit.php?filename=tryjs_object_method)

[函数属性作为一个属性访问](https://www.runoob.com/try/tryit.php?filename=tryjs_object_function)

### JavaScript 函数

函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块.

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>测试实例</title>
<script>
function myFunction()
{
    alert("Hello World!");
}
</script>
</head>
 
<body>
<button onclick="myFunction()">点我</button>
</body>
</html><!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>测试实例</title>
<script>
function myFunction()
{
    alert("Hello World!");
}
</script>
</head>
 
<body>
<button onclick="myFunction()">点我</button>
</body>
</html>
```

### JavaScript 函数语法

函数就是包裹在花括号中的代码块,前面使用了关键词 function:

```
function functionname()
{
    // 执行代码
}
```

当调用函数时,会执行函数内的代码.

可以在某事件发生时直接调用函数 (比如当用户点击按钮时),并且可由 JavaScript 在任何位置进行调用.

***JavaScript 对大小写敏感.关键词 function 必须是小写的,并且必须以与函数名称相同的大小写来调用函数.***

### 调用带参数的函数

在调用函数时,可以向其传递值,这些值被称为参数.

这些参数可以在函数中使用.

可以发送任意多的参数,由逗号 (,) 分隔:

```
myFunction(argument1,argument2)
```

当声明函数时,请把参数作为变量来声明:

```
function myFunction(var1,var2)
{
代码
}
```

变量和参数必须以一致的顺序出现.第一个变量就是第一个被传递的参数的给定的值,以此类推.

```
<p>点击这个按钮，来调用带参数的函数。</p>
<button onclick="myFunction('Harry Potter','Wizard')">点击这里</button>
<script>
function myFunction(name,job){
    alert("Welcome " + name + ", the " + job);
}
</script>
```

上面的函数在按钮被点击时会提示 "Welcome Harry Potter,the Wizard".

函数很灵活,可以使用不同的参数来调用该函数,这样就会给出不同的消息:

```
<button onclick="myFunction('Harry Potter','Wizard')">点击这里</button>
<button onclick="myFunction('Bob','Builder')">点击这里</button>
```

根据点击的不同的按钮,上面的例子会提示 "Welcome Harry Potter,the Wizard" 或 "Welcome Bob,the Builder".

### 带有返回值的函数

有时,我们会希望函数将值返回调用它的地方.

通过使用 return 语句就可以实现.

在使用 return 语句时,函数会停止执行,并返回指定的值.

**语法**

```
function myFunction()
{
    var x=5;
    return x;
}
```

上面的函数会返回值 5.

***注意:*** 整个 JavaScript 并不会停止执行,仅仅是函数.JavaScript 将继续执行代码,从调用函数的地方.

函数调用将被返回值取代:

```
var myVar=myFunction();
```

myVar 变量的值是 5,也就是函数 "myFunction()" 所返回的值.

即使不把它保存为变量,也可以使用返回值:

```
document.getElementById("demo").innerHTML=myFunction();
```

"demo" 元素的 innerHTML 将成为 5,也就是函数 "myFunction()" 所返回的值.

可以使返回值基于传递到函数中的参数:

```
function myFunction(a,b)
{
    return a*b;
}
 
document.getElementById("demo").innerHTML=myFunction(4,3);
```

"demo" 元素的 innerHTML 将是:

12

在我们仅仅希望退出函数时,也可使用 return 语句.返回值是可选的:

```
function myFunction(a,b)
{
    if (a>b)
    {
        return;
    }
    x=a+b
}
```

如果 a 大于 b,则上面的代码将退出函数,并不会计算 a 和 b 的总和.

### 局部 JavaScript 变量

在 JavaScript 函数内部声明的变量 (使用 var) 是局部变量,所以只能在函数内部访问它. (该变量的作用域是局部的).

我们可以在不同的函数中使用名称相同的局部变量,因为只有声明过该变量的函数才能识别出该变量.

只要函数运行完毕,本地变量就会被删除.

### 全局 JavaScript 变量

在函数外声明的变量是全局变量,网页上的所有脚本和函数都能访问它.

### JavaScript 变量的生存期

JavaScript 变量的生命周期从它们被声明的时间开始.

局部变量会在函数运行以后被删除.

全局变量会在页面关闭后被删除.

### 向未声明的 JavaScript 变量分配值

如果我们把值赋给尚未声明的变量,该变量将被自动作为 window 的一个属性.

这条语句:

```
carname="Volvo";
```

将声明 window 的一个属性 carname.

非严格模式下给未声明变量赋值创建的全局变量,是全局对象的可配置属性,可以删除.

```
var var1 = 1; // 不可配置全局属性
var2 = 2; // 没有使用 var 声明，可配置全局属性

console.log(this.var1); // 1
console.log(window.var1); // 1
console.log(window.var2); // 2

delete var1; // false 无法删除
console.log(var1); //1

delete var2; 
console.log(delete var2); // true
console.log(var2); // 已经删除 报错变量未定义
```

## JavaScript 作用域

作用域是可访问变量的集合.

### JavaScript 作用域

在 JavaScript 中,对象和函数同样也是变量.

**在 JavaScript 中,作用域为可访问变量,对象,函数的集合.**

JavaScript 函数作用域:作用域在函数内修改.

### JavaScript 局部作用域

变量在函数内声明,变量为局部变量,具有局部作用域.

局部变量:只能在函数内部访问.

```
// 此处不能调用 carName 变量
function myFunction() {
    var carName = "Volvo";
    // 函数内可调用 carName 变量
}
```

因为局部变量只作用于函数内,所以不同的函数可以使用相同名称的变量.

局部变量在函数开始执行时创建,函数执行完后局部变量会自动销毁.

### JavaScript 全局变量

变量在函数外定义,即为全局变量.

全局变量有 **全局作用域**:网页中所有脚本和函数均可使用.

```
var carName = " Volvo";
 
// 此处可调用 carName 变量
function myFunction() {
    // 函数内可调用 carName 变量
}
```

如果变量在函数内没有声明 (没有使用 var 关键字),该变量为全局变量.

以下实例中 carName 在函数内,但是为全局变量.

```
// 此处可调用 carName 变量
 
function myFunction() {
    carName = "Volvo";
    // 此处可调用 carName 变量
}
```

### JavaScript 变量生命周期

JavaScript 变量生命周期在它声明时初始化.

局部变量在函数执行完毕后销毁.

全局变量在页面关闭后销毁.

### 函数参数

函数参数只在函数内起作用,是局部变量.

### HTML 中的全局变量

在 HTML 中,全局变量是 window 对象,所以 window 对象可以调用函数内的未声明 (未加 var) 的局部变量.

**注意:** 所有全局变量都属于 window 对象.

```
//此处可使用 window.carName
 
function myFunction() {
    carName = "Volvo";
}
```

### 你知道吗?

***你的全局变量,或者函数,可以覆盖 window 对象的变量或者函数.***

***局部变量,包括 window 对象可以覆盖全局变量和函数.***

在 JavaScript 中,函数内部的局部变量通常不可以直接被外部访问,但有几种方式可以将函数内部的局部变量暴露给外部作用域,具体如下:

- **通过全局对象:** 在函数内部,可以通过将局部变量赋值给 window 对象的属性来使其成为全局可访问的.例如,使用 **window.a = a;** 语句,可以在函数外部通过 **window.a** 访问到这个局部变量的值

- **定义全局变量:** 在函数内部不使用 **var、let** 或 **const** 等关键字声明变量时，该变量会被视为全局变量，从而可以在函数外部访问。但这种做法通常不推荐，因为它可能导致意外的副作用和代码难以维护。

- **返回值:** 可以通过在函数内部使用 **return** 语句返回局部变量的值,然后在函数外部接收这个返回值.这样,虽然局部变量本身不会被暴露,但其值可以通过函数调用传递到外部.

- **闭包:** JavaScript 中的闭包特性允许内部函数访问外部函数的局部变量.即使外部函数执行完毕后,其局部变量仍然可以被内部函数引用.

- **属性和方法:** 定义在全局作用域中的变量和函数都会变成 window 对象的属性和方法,因此可以在调用时省略 window,直接使用变量名或函数名.

## JavaScript 事件

HTML 事件是发生在 HTML 元素上的事情.

挡在 HTML 页面中使用 JavaScript 时,JavaScript 可以触发这些事件.

### HTML 事件

HTML 事件可以是浏览器行为,也可以是用户行为.

以下是 HTML 事件的实例:

- HTML 页面完成加载

- HTML input 字段改变时

- HTML 按钮被点击

通常,当事件发生时,可以做这些事情.

在事件触发时 JavaScript 可以执行一些代码.

HTML 元素中可以添加事件属性,使用 JavaScript 代码来添加 HTML 元素.

单引号:

```
<some-HTML-element some-event='JavaScript 代码'>
```

双引号:

```
<some-HTML-element some-event="JavaScript 代码">
```

在以下实例中,按钮元素中添加了 onclick 属性 (并加上代码):

```
<button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
```

以上实例中,JavaScript 代码将修改 id="demo" 元素的内容.

在下一个实例中,代码将修改自身元素的内容 (使用 **this**.innerHTML):

```
<button onclick="this.innerHTML=Date()">现在的时间是?</button>
```

*** JavaScript 代码通常是几行代码.比较常见的是通过事件属性来调用:***

```
<button onclick="displayDate()">现在的时间是?</button>
```

### 常见的 HTML 事件

下面是一些常见的 HTML 事件的列表:

|事件|描述|
|:---:|:---:|
|onchange|HTML 元素改变|
|onclick|用户点击 HTML 元素|
|onmouseover|鼠标指针移动到指定的元素上时发生|
|onmouseout|用户从一个 html 元素上移开鼠标时发生|
|onkeydown|用户按下键盘按键|
|onload|浏览器已完成页面的加载|

更多事件列表: [JavaScript 参考手册 - HTML DOM 事件](https://www.runoob.com/jsref/dom-obj-event.html).

### JavaScript 可以做什么?

事件可以用于处理表单验证,用户输入,用户行为及浏览器动作:

- 页面加载时触发事件

- 页面关闭时触发事件

- 用户点击按钮执行动作

- 验证用户输入内容的合法性

- 等等...

可以使用多种方法来执行 JavaScript 事件代码:

- HTML 事件属性可以直接执行 JavaScript 代码

- HTML 事件属性可以调用 JavaScript 函数

- 可以为 HTML 元素指定自己的事件处理程序

- 可以阻止事件的发生.

- 等等...

***在 HTML DOM 章节中将会学到更多关于事件及事件处理程序的知识.***

## JavaScript 字符串

JavaScript 字符串用于存储和处理文本.

### JavaScript 字符串

字符串可以存储一系列字符,如 "John Doe".

字符串可以是插入到引号中的任何字符.可以使用单引号或双引号:

```
var
carname = "Volvo XC60";
var
carname = 'Volvo XC60';
```

可以使用索引位置来访问字符串中的每个字符:

```
var character = carname[7];
```

字符串的索引从 0 开始,这意味着第一个字符索引值为 `[0]`,第二个为`[1]`,以此类推.

```
const name = "RUNOOB";
let letter = name[2];

document.getElementById("demo").innerHTML = letter;
```

可以在字符串中使用引号,字符串中的引号不要与字符串的引号相同:

```
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
```

也可以在字符串添加转义符来使用引号:

```
var x = 'It\'s alright';
var y = "He is called \"Johnny\"";
```

### 字符串长度

可以使用内置属性 length 来计算字符串的长度:

```
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";var sln = txt.length;
```

### 特殊字符

在 JavaScript 中,字符串写在单引号或双引号中.

因为这样,以下实例 JavaScript 无法解析:

```
"We are the so-called "Vikings" from the north."
```

字符串 "We are the so-called" 被截断.

如何解决以上问题呢?可以使用反斜杠 (\) 来转义 "Vikings" 字符串中的双引号,若下:

```
"We are the so-called \"Vikings\" from the north."
```

反斜杠是一个**转义字符**.转义字符将特殊字符转换为字符串字符:

转义字符 (\) 可以用于转义撇号,换行,引号,等其他特殊字符:

|代码|输出|
|:---:|:---:|
|\'|单引号|
|\"|双引号|
|\\|反斜杠|
|\n|换行|
|\r|回车|
|\t|tab (制表符)|
|\b|退格符|
|\f|换页符|

### 字符串可以是对象

通常, JavaScript 字符串是原始值,可以使用字符创建: **var firstName = "John"**

但我们也可以使用 new 关键字将字符串定义为一个对象: **var firstName = new String("John")

```
var x = "John";
var y = new String("John");
typeof x //  返回 String
typeof y // 返回 Object
```

***不要创建 String 对象.它会拖慢执行速度,并可能产生其他副作用:***

```
var x = "John";              
var y = new String("John");
(x === y) // 结果为 false，因为 x 是字符串，y 是对象var x = "John";              
var y = new String("John");
(x === y) // 结果为 false，因为 x 是字符串，y 是对象
```

=== 为绝对相等,即数据类型与值都必须相等.

### 字符串属性和方法

原始值字符串,如 "John",没有属性和方法(因为他们不是对象).

原始值可以使用 JavaScript 的属性和方法,因为 JavaScript 在执行方法和属性时可以吧原始值当作对象.

**字符串方法我们将在下一章节中介绍**

### 字符串属性

|属性|描述|
|:---:|:---:|
|constructor|返回创建字符串属性的函数|
|length|返回字符串的长度|
|prototype|允许向对象添加属性和方法|

### 字符串方法

更多方法实例可以参见: [JavaScript String 对象](https://www.runoob.com/jsref/jsref-obj-string.html).

|方法|描述|
|:---:|:---:|
|charAt()|返回指定索引位置的字符|
|charCodeAt()|返回指定索引位置字符 Unicode 值|
|concat()|连接两个或多个字符串,返回连接后的字符串|
|fromCharCode()|将 Unicode 转换为字符串|
|indexOf()|返回字符串中检索指定字符第一次出现的位置|
|lastIndexOf()|返回字符串中检索指定字符最后一次出现的位置|
|localeCompare()|用本地特定的顺序来比较连个字符串|
|match()|找到一个或多个正则表达式的匹配|
|replace()|替换与正则表达式匹配的子串|
|search()|检索与正则表达式相匹配的值|
|slice()|提取字符串的片段,并在新的字符串中返回被提取的部分|
|split()|吧字符串分割为子字符串的数组|
|substr()|从起始索引号提取字符串中指定数目的字符|
|substring()|提取字符串中两个指定的索引号之间的字符|
|toLocaleLowerCase()|根据主机的语言环境把字符串转换为小写,只有几种语言 (如土耳其语) 具有地方特有的大小写映射|
|toLocaleUpperCase()|根据主机的语言环境把字符串转换为大写,只有几种语言 (如土耳其语) 具有地方特有的大小写映射|
|toLowerCase()|把字符串转换为小写|
|toString()|返回字符串对象值|
|toUpperCase()|把字符串转换为大写|
|trim()|移除字符串首位空白|
|valueOf()|返回某个字符串对象的原始值|

## JavaScript 字符串模板

### JavaScript 模板字符串

JavaScript 中的模板字符串是一种方便的字符串语法,允许在字符串中嵌入表达式和变量.

模板字符串使用单引号 `` 作为字符串的定界符分隔的字面量.

模板字面量是用单引号 (`) 分隔的字面量,允许多行字符串、带嵌入表达式的字符串插值和一种叫带标签的模板的特殊结构

**语法**

```
`string text`

`string text line 1
 string text line 2`

`string text ${expression} string text`

tagFunction`string text ${expression} string text`
```

**参数**

- **string text:** 将成为模板字面量的一部分的字符串文本.几乎允许所有字符,包括换行符和其他空白字符.但是,除非使用了标签函数,否则无效的转义序列将导致语法错误.

- **expression:** 要插入当前位置的表达式,其值被转换为字符串或传递给 tagFunction.

- **tagFunction:** 如果指定,将使用模板字符串数组和替换表达式调用它,返回值将成为模板字面量的值.

```
let text = `Hello RUNOOB!`;
```

**浏览器支持**

Chrome,Edge,Firefox,Safari,Opera

模板字符串中可以同时使用单引号和双引号:

```
let text = `He's often called "Runoob"`;
```

模板字符串还支持多行文本,而无需使用特殊的转义字符;

```
const multiLineText = `
  This is
  a multi-line
  text.
`;
```

若要转义模板字面量中的反引号 (\`),需在反引号之前加一个反斜杠 (\\).

```
`\`` === "`"; // true
```

模板字面量用反引号 (\`) 扩起来,二部是双引号 (") 或单引号 (') .

除了普通字符串外,模板字面量还可以包含占位符 ———— 一种由美元符号和大括号分隔的嵌入式表达式： **${expression}**.

字符串和占位符被传递给一个函数 (要么是默认函数,要么是自定义函数).默认函数 (当未提供自定义函数时) 只执行字符串插值来替换占位符,然后将这些部分拼接到一个字符串中.

模板字符串中允许我们使用变量:

```
const name = 'Runoob';
const age = 30;
const message = `My name is ${name} and I'm ${age} years old.`;
```

以上实例中,**${name}** 和 **${age}** 是模板字符串的表达式部分,它们被包含在 **${}** 内部,并在运行时求值.

模板字符串允许我们在字符串中引用变量、执行函数调用和进行任意的 JavaScript 表达式.

模板字符串中允许我们使用表达式:

```
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

模板字符串当作 HTML 模板使用:

```
let header = "";
let tags = ["RUNOOB", "GOOGLE", "TAOBAO"];

let html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```

## JavaScript 运算符

**运算符 = 用于赋值**

**运算符 + 用于加值**

运算符 = 用于给 JavaScript 变量赋值.

算术运算符 **+** 用于把值加起来.

```
y=5;
z=2;
x=y+z;
```

以上语句执行后,x 的值是:

7

### JavaScript 算术运算符

与 / 或 值之间的算术运算符.

**y=5**,下面的表格解释了这些算术运算符:

|运算符|描述|例子|x 运算结果|y 运算结果|在线实例|
|:---:|:---:|:---:|:---:|:---:|:---:|
|+|加法|x=y+2|7|5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_add)|
|-|减法|x=y-2|3|5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_sub)|
|*|乘法|x=y*2|10|5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_mult)|
|/|除法|x=y/2|2.5|5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_div)|
|%|取模 (余数)|x=y%2|1|5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_mod)|
|++|自增|x=++y|6|6|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_incr)|
|++|自增|x=y++|5|6|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_incr2)|
|--|自减|x=--y|4|4|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_decr)|
|--|自减|x=--y|5|4|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_decr2)|

### JavaScript 赋值运算符

赋值运算符用于给 JavaScript 变量赋值.

给定 **x=10** 和 **y=5**,下面的表格解释了赋值运算符:

|运算符|例子|等同于|运算结果|在线实例|
|:---:|:---:|:---:|:---:|:---:|
|=|x=y||x=5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_equal)|
|+=|x+=y|x=x+y|x=15|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_plusequal)|
|-=|x-=y|x=x-y|x=5|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_minequal)|
|*=|x*=y|x=x*y|x=50|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_multequal)|
|/=|x/=y|x=x/y|x=2|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_divequal)|
|%=|x%=y|x=x%y|x=0|[实例](https://www.runoob.com/try/try.php?filename=tryjs_oper_modequal)|

### 用于字符串的 + 运算符

**+** 运算符用于把文本值或字符串变量加起来 (连接起来).

如需把两个或多个字符串变量连接起来,请使用 **+** 运算符.

```
txt1="What a very";
txt2="nice day";
txt3=txt1+txt2;
```

txt3 运算结果如下:

What a verynice day

要想在两个字符串之间增加空格,需要把空格插入一个字符串之中:

```
txt1="What a very ";
txt2="nice day";
txt3=txt1+txt2;
```

在以上语句执行后,变量 txt3 包含的值是:

What a very nice day

### 对字符串和数字进行加法运算

两个数字相加,返回数字相加的和,若果数字与字符串相加,返回字符串,如下实例:

```
x=5+5;
y="5"+5;
z="Hello"+5;
```

x,y,和 z 输出结果为:

```
10
55
Hello5
```

**规则**:如果把数字与字符串相加,结果将成为字符串!

## JavaScript 比较



















