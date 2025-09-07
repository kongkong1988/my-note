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

### JavaScript 语法
