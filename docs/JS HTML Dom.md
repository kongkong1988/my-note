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

## JavaScript HTML DOM 改变 HTML 内容

HTML DOM 允许 JavaScript 改变 HTML 元素的内容.

### 改变 HTML 输出流

JavaScript 能够创建动态的 HTML 内容:


 
