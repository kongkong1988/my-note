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

```
onclick=JavaScript
```

HTML 事件的例子:

- 当用户点击鼠标时

- 当网页已加载时

- 当图像已加载时

- 当鼠标移动到元素上时

- 当输入字段被改变时

- 当提交 HTML 表单时

- 当用户触发按键时

在本例中,当用户在`<h1>`元素上点击时,会改变其内容:

```
<!DOCTYPE html><html>
<body>
<h1 onclick="this.innerHTML='Ooops!'">点击文本!</h1>
</body>
</html>
```

本例从事件处理器调用一个函数:

```
<!DOCTYPE html><html>
<head>
<script>
function changetext(id)
{
    id.innerHTML="Ooops!";
}
</script>
</head>
<body>
<h1 onclick="changetext(this)">点击文本!</h1>
</body>
</html>
```

### HTML 事件属性

如需向 HTML 元素分配事件,可以使用事件属性.

```
<button onclick="displayDate()">点这里</button>
```

在上面的例子中,名为 displayDate 的函数将在按钮被点击时执行.

### 使用 HTML DOM 来分配事件

HTML DOM 允许使用 JavaScript 来向 HTML 元素分配事件:

```
<script>
document.getElementById("myBtn").onclick=function(){displayDate()};
</script>
```

在上面的例子中,名为 displayDate 的函数被分配给 id="myBtn" 的 HTML 元素.

按钮点击时 JavaScript 函数将会被执行.

### onload 和 onunload 事件

onload 和 onunload 事件会在用户进入或离开页面时被触发。

onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

onload 和 onunload 事件可用于处理 cookie。

```
<body onload="checkCookies()">
```

### onchange 事件

onchange 事件常结合对输入字段的验证来使用。

下面是一个如何使用 onchange 的例子。当用户改变输入字段的内容时，会调用 upperCase() 函数。

```
<input type="text" id="fname"onchange="upperCase()">
```

### onmouseover 和 onmouseout 事件

[onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。](https://www.runoob.com/js/js-htmldom-events.html)


### onmousedown、onmouseup 以及 onclick 事件

[onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。](https://www.runoob.com/js/js-htmldom-events.html)

### 更多实例

[onmousedown 和onmouseup](https://www.runoob.com/try/try.php?filename=trydhtml_event_onmousedown)

当用户按下鼠标时,更换一幅图像.

[onload](https://www.runoob.com/try/try.php?filename=trydhtml_event_onload)

当页面完成加载时,显示一个提示框.

[onfocus](https://www.runoob.com/try/try.php?filename=tryjsref_onfocus)

当输入字段获得焦点时,改变其背景色.

[鼠标事件](https://www.runoob.com/try/try.php?filename=trydhtml_event_onmouse)

当指针移动到元素上方时,改变其颜色;当指针移出文本后,会再次改变其颜色.

## DOM EventListener

### addEventListener() 方法

```
document.getElementById("myBtn").addEventListener("click", displayDate);
```

addEventListener() 方法用于向指定元素添加事件句柄。

addEventListener() 方法添加的事件句柄不会覆盖已存在的事件句柄。

你可以向一个元素添加多个事件句柄。

你可以向同个元素添加多个同类型的事件句柄，如：两个 "click" 事件。

你可以向任何 DOM 对象添加事件监听，不仅仅是 HTML 元素。如： window 对象。

addEventListener() 方法可以更简单的控制事件（冒泡与捕获）。

当你使用 addEventListener() 方法时, JavaScript 从 HTML 标记中分离开来，可读性更强， 在没有控制HTML标记时也可以添加事件监听。

你可以使用 removeEventListener() 方法来移除事件的监听。

### 语法

```
element.addEventListener(event, function, useCapture);
```

***注意:不要使用"on"前缀.例如,使用"click",而不是使用"onclick".***

### 向元素添加事件句柄

```
element.addEventListener("click", function(){ alert("Hello World!"); });
```

可以使用函数名,来引用外部函数:

```
element.addEventListener("click", myFunction);

function myFunction() {    
		alert ("Hello World!");
}
```

### 向同一个元素中添加多个事件句柄

addEventListener() 方法允许向同一个元素添加多个事件，且不会覆盖已存在的事件：

```
element.addEventListener("click", myFunction);element.addEventListener("click", mySecondFunction);
```

可以向同个元素添加不同类型的事件：

```
element.addEventListener("mouseover", myFunction);
element.addEventListener("click", mySecondFunction);
element.addEventListener("mouseout", myThirdFunction);
```

### 向 Window 对象添加事件句柄

addEventListener() 方法允许你在 HTML DOM 对象添加事件监听， HTML DOM 对象如： HTML 元素, HTML 文档, window 对象。或者其他支持的事件对象如: xmlHttpRequest 对象。

```
window.addEventListener("resize", function(){
    document.getElementById("demo").innerHTML = sometext;
});
```

###传递参数

当传递参数时,使用'匿名函数'调用带参数的函数:

```
element.addEventListener("click", function(){ myFunction(p1, p2); });
```

### 事件冒泡或事件捕获?

事件传递有两种方式：冒泡与捕获。

事件传递定义了元素事件触发的顺序。 如果你将 <p> 元素插入到 <div> 元素中，用户点击 <p> 元素, 哪个元素的 "click" 事件先被触发呢？

在 冒泡 中，内部元素的事件会先被触发，然后再触发外部元素，即： <p> 元素的点击事件先触发，然后会触发 <div> 元素的点击事件。

在 捕获 中，外部元素的事件会先被触发，然后才会触发内部元素的事件，即： <div> 元素的点击事件先触发 ，然后再触发 <p> 元素的点击事件。

addEventListener() 方法可以指定 "useCapture" 参数来设置传递类型：

    addEventListener(event, function, useCapture);   

默认值为 false, 即冒泡传递，当值为 true 时, 事件使用捕获传递。

```
document.getElementById("myDiv").addEventListener("click", myFunction, true);
```

### removeEventListener() 方法

removeEventListener() 方法移除由 addEventListener() 方法添加的事件句柄:

```
element.removeEventListener("mousemove", myFunction);
```

### HTML DOM 事件对象参考手册

所有 HTML DOM 事件,可以查看完整的[HTML DOM Event 对象参考手册](https://www.runoob.com/jsref/dom-obj-event.html).
