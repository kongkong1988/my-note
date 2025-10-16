## DOM 简介

### JavaScript HTML DOM

通过 HTML DOM,可以访问 JavaScript HTML 文档的所有元素.

### HTML DOM (文档对象模型)

当网页被加载时,浏览器会创建页面的文档对象模型 (Document Object Model).

**HTML DOM** 模型被构造**对象**的树:

![](./img/pic_htmltree.gif)

通过可编程的对象模型,JavaScript 获得了足够的能力来创建动态的 HTML.

- JavaScript 能够改变页面中的所有 HTML 元素

- JavaScript 能够改变页面中的所有 HTML 属性

- JavaScript 能够改变页面中的所有 CSS 样式

- JavaScript 能够对页面中的所有事件做出反应

### 查找 HTML 元素

通常,通过 JavaScript,我们需要操作 HTML 元素.

为了做到这件事情,我们必须首先找到该元素.有三种方法来做这件事:

- 通过 id 找到 HTML 元素

- 通过标签名找到 HTML 元素

- 通过类名找到 HTML 元素

### 通过 id 查找 HTML 元素

在 DOM 中查找 HTML 元素的最简单方法,是通过使用元素的 id.

本例查找 id="intro" 元素:

```
var x=document.getElementById("intro");
```

如果找到该元素,则该方法将以对象 (在 x 中) 的形式返回该元素.

如果未找到该元素,则 x 将包含 null.

### 通过标签名查找 HTML 元素

本例查找 id="main" 的元素,然后查找 id="main" 元素中的所有 '<p>' 元素:

```
var x=document.getElementById("main");
var y=x.getElementsByTagName("p");
```

### 通过类名找到 HTML 元素

本例通过 **getElementsByClassName** 函数来查找 class='intro'的元素:

```
var x=document.getElementsByClassName("intro");
```

### HTML DOM 教程

在本教程接下来的篇幅中,将学到:

- 如何改变 HTML 元素的内容 (innerHTML)

- 如何改变 HTML 元素的样式 (CSS)

- 如何对 HTML DOM 事件做出反应

- 如何添加或删除 HTML 元素

## JavaScript HTML DOM 改变 - HTML 内容

HTML DOM 允许 JavaScript 改变 HTML 元素的内容.

### 改变 HTML 输出流

JavaScript 能够创建动态的 HTML 内容:

### 改变 HTML 输出流
 
JavaScript 能够创建动态的 HTML 内容.

在 JavaScript 中,document.write() 可用于直接想 HTML 输出流写内容.

```
<!DOCTYPE html><html>
<body>
<script>
document.write(Date());
</script>
</body>
</html>
```

***绝对不要在文档(DOM)加载完成后使用 document.write().这会覆盖该文档.

### 改变 HTML 内容

修改 HTML 内容的最简单的方法是使用 innerHTML 属性.

如需改变 HTML 元素的内容,请使用这个语法:

    document.getElementById(id).innerHTML=新的 HTML

本例改变了`<p>`元素的内容:

```
<html>
<body>
<p id="p1">Hello World!</p>
<script>
document.getElementById("p1").innerHTML="新文本!";
</script>
</body>
</html>
```

本例改变了`<h1>`元素的内容:

```
<!DOCTYPE html><html>
<body>
<h1 id="header">Old Header</h1>
<script>
	var element=document.getElementById("header");element.innerHTML="新标题";
</script>
</body>
</html>
```

实例讲解:

- 上面的 HTML 文档含有 id="header"的`<h1>`元素

- 我们使用 HTML DOM 来获得 id="header"的元素

- JavaScript 更改次元素的内容(innerHTML)

### 改变 HTML 属性

如需改变 HTML 元素的属性,请使用这个语法:

    document.getElementById(id).attribute=新属性值

本例改变了 `<img>` 元素的 src 属性:

```
<!DOCTYPE html><html>
<body>
<img id="image" src="smiley.gif">
<script>
document.getElementById("image").src="landscape.jpg";
</script>
</body>
</html>
```

实例讲解:

- 上面的HTML 文档含有 id="image"的`<img>`元素

- 我们使用 HTML DOM 来获得 id="image"的元素

- JavaScript 更改次元素的属性 (把"smiley.gif"改为"landscape.jpg")

## JavaScript HTML DOM 改变 CSS

HTML DOM 允许 JavaScript 改变 HTML 元素的样式.

### 改变 HTML 样式

如需改变 HTML 元素的样式,请使用这个语法:

    document.getElementById(id).style.property=新样式

下面的例子会改变 `<p>` 元素的样式:

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>
 
<p id="p1">Hello World!</p>
<p id="p2">Hello World!</p>
<script>
document.getElementById("p2").style.color="blue";
document.getElementById("p2").style.fontFamily="Arial";
document.getElementById("p2").style.fontSize="larger";
</script>
<p>以上段落通过脚本修改。</p>
 
</body>
</html>
```

### 使用事件

HTML DOM 允许我们通过出发事件来执行代码.

比如以下事件:

- 元素被点击

- 页面加载完成

- 输入框被修改.

- ......

本例改变了 id="id1" 的 HTML 元素的样式,当用户点击按钮时:

```
<!DOCTYPE html><html><body><h1 id="id1">我的标题 1</h1>
	<button type="button" onclick="document.getElementById('id1').style.color='red'">
	点我!</button></body></html>
```

## JavaScript HTML DOM 事件

HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应.

[实例](https://www.runoob.com/js/js-htmldom-events.html)

### 对事件做出反应

我们可以在事件发生时执行 JavaScript,比如当用户在 HTML 元素上点击时.

如需在用户点击某个元素时执行代码,请向一个 HTML 事件属性添加 JavaScript 代码:

    
