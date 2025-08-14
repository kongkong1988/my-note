# CSS入门教程

## CSS 样式基础

- 指南:

  - [层叠与继承](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Handling_conflicts)
 
    - 层叠、优先级和继承——这三个基本的 CSS 概念的理解
   
    - 这些概念控制着 CSS 如何应用于 HTML 以及应用时的优先顺序
 
  - [CSS 选择器](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
 
    - [类型、类以及 ID 选择器](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
   
    - [属性选择器](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
   
    - [伪类与伪元素](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
   
    - [关系选择器](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
 
  - 盒模型
 
    - 所有 CSS 都是包在盒子里的，那么理解这些盒子就是让我们能够创建 CSS 布局或排列元素的关键点了。为了接下来能完成编写复杂布局的任务，本节我们会认真看看CSS 盒模型，了解其原理及相关术语。
 
  - 背景与边框
 
    - 在这一节课中，我们将会看一下你可以用 CSS 对背景和边框进行哪些创新。通过添加渐变、背景图片和圆角，背景和边框可以解决许多 CSS 中的样式问题。
 
  - 处理不同的文本方向
 
    - 最近几年来，CSS 进行了演化，以更好地支持不同方向的内容，既包括自左至右，又包括自上至下（如日语）的内容——这些不同的排布方向被称作书写模式。随着你在这部分学习中不断前进并开始设计网页布局，理解书写模式将会非常有帮助，因此我们会在本文中进行介绍。
 
  - 溢出的内容
 
    - 这一节我们会关注 CSS 中的另一个重要的概念——溢出。溢出发生在一个盒子中包含了过多内容以致超出适当的范围时。在这篇指南中，你将学到什么是溢出以及如何处理它。
 
  - 值和单位
 
    - CSS 中每一个属性都有一个取值或者一系列合理的取值。这一节，我们将了解一些最常用的取值和单位。
 
  - 在 CSS 中调整大小
 
    - 通过目前为止的一系列课程，你已经了解了许多使用 CSS 调整网页项目大小的方法。了解你所设计的不同特性将呈现的大小很重要，我们将在这节课中总结使用 CSS 调整大小的不同方法，并定义几个有关尺寸的术语，这将对你有所帮助。
 
  - 图片、媒体和表单元素
 
    - 在这一节，我们会了解 CSS 是如何处理一些特殊元素的。与常规的盒子相比，图片、其他媒体和表格元素对你使用 CSS 设置样式的能力提出了不同的要求。理解什么能够实现和什么不能够实现将会免去你一些沮丧，这节课会突出一些你需要了解的主要问题。
 
  - 样式化表格
 
    - 设计 HTML 表格的样式并不是多么美妙的工作，但有时却是我们都需要去做的。这篇文章通过突出一些特定的表格样式技巧，为设计好看的 HTML 表格提供了一份指南。
 
  - 调试 CSS
 
    - 有时在编写 CSS 的过程中，你会遇到这样一个问题：你的 CSS 并没有实现你想要的效果。这篇文章将为你提供指导，教你如何调试 CSS 问题，以及如何使用所有现代浏览器带有的开发者工具找到问题所在。
 
  - 组织 CSS
 
    - 当你开始处理更大的样式表和项目时，你将会发现维护一个庞大的样式表非常具有挑战性。在这篇文章中，我们将会简要了解使得 CSS 易于维护的最佳做法，以及其他人所使用的一些有助于增进可维护性的解决方案。

### CSS 如何运行

 - 前置知识：基础计算知识、基本软件安装、简单文件知识、HTML 基础
 
 - 目标：理解浏览器如何加载 CSS 和 HTML、浏览器遇到无法解析的 CSS 会发生什么
 
- CSS 究竟是怎么工作的？
  
  1. 浏览器载入 HTML 文件（比如从网络上获取）。
  2. 将 HTML 文件转化成一个 DOM（Document Object Model），DOM 是文件在计算机内存中的表现形式，下一节将更加详细的解释 DOM。
  3. 接下来，浏览器会拉取该 HTML 相关的大部分资源，比如嵌入到页面的图片、视频和 CSS 样式。JavaScript 则会稍后进行处理，简单起见，同时此节主讲 CSS，所以这里对如何加载 JavaScript 不会展开叙述。
  4. 浏览器拉取到 CSS 之后会进行解析，根据选择器的不同类型（比如 element、class、id 等等）把他们分到不同的“桶”中。浏览器基于它找到的不同的选择器，将不同的规则（基于选择器的规则，如元素选择器、类选择器、id 选择器等）应用在对应的 DOM 的节点中，并添加节点依赖的样式（这个中间步骤称为渲染树）。
  5. 上述的规则应用于渲染树之后，渲染树会依照应该出现的结构进行布局。
  6. 网页展示在屏幕上（这一步被称为着色）。

- 关于 DOM

  - 一个 DOM 有一个树形结构，标记语言中的每一个元素、属性以及每一段文字都对应着结构树中的一个节点（Node/DOM 或 DOM node）。节点由节点本身和其他 DOM 节点的关系定义，有些节点有父节点，有些节点有兄弟节点（同级节点）。
 
- 一个真实的 DOM 案例

HTML

```
<p>
  Let's use:
  <span>Cascading</span>
  <span>Style</span>
  <span>Sheets</span>
</p>
```

在这个 DOM 中，<p>元素对应了父节点，它的子节点是一个 text 节点和三个对应了`<span>`元素的节点，SPAN节点同时也是他们中的 Text 节点的父节点。

```
P
├─ "Let's use:"
├─ SPAN
|  └─ "Cascading"
├─ SPAN
|  └─ "Style"
└─ SPAN
    └─ "Sheets"
```

上图就是浏览器怎么解析之前那个 HTML 片段——它生成上图的 DOM 树形结构并将它按照如下输出到浏览器：

```
Let's use: Cascading Style Sheets
```

- 应用 CSS 到 DOM

接下来让我们看看添加一些 CSS 到文件里加以渲染，同样的 HTML 代码：

HTML

```
<p>
  Let's use:
  <span>Cascading</span>
  <span>Style</span>
  <span>Sheets</span>
</p>
```

```
span {
  border: 1px solid black;
  background-color: lime;
}
```

浏览器会解析 HTML 并创造一个 DOM，然后解析 CSS。可以看到唯一的选择器就是span元素选择器，浏览器处理规则会非常快！把同样的规则直接使用在三个`<span>`标签上，然后渲染出图像到屏幕。

```
Let's use: Cascading Style Sheets
```

- 当浏览器遇到无法解析的 CSS 代码会发生什么

  - 答案就是浏览器什么也不会做，继续解析下一个 CSS 样式！

### 开始 CSS 的学习之旅

- 目标：

  - 理解 HTML 文档链接 CSS 文档的几个基本套路
 
  - 能运用 CSS 做些文字上的格式化操作

- 先从下面这段 HTML 开始

HTML

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>开始学习 CSS</title>
  </head>

  <body>
    <h1>我是一级标题</h1>

    <p>
      这是一个段落文本。在文本中有一个 <span>span element</span> 并且还有一个
      <a href="http://example.com">链接</a>.
    </p>

    <p>这是第二段。包含了一个 <em>强调</em> 元素。</p>

    <ul>
      <li>项目 1</li>
      <li>项目 2</li>
      <li>项目 <em>三</em></li>
    </ul>
  </body>
</html>
```
- 添加 CSS 代码

  - 有三种方式可以实现，而目前我们更倾向于利用最普遍且有用的方式——在文档的开头链接 CSS。
 
  - 在 HTML 文档的相同目录创建一个文件，保存并命名为 styles.css 。
 
  - 为了把 styles.css 和 index.html 连接起来，可以在 HTML 文档中，`<head>` 语句模块里面加上下面的代码：
 
HTML

```
<link rel="stylesheet" href="styles.css" />
```

```
<link> 语句块里面，我们用属性 rel，让浏览器知道有 CSS 文档存在（所以需要遵守 CSS 样式的规定），并利用属性 href 指定，寻找 CSS 文件的位置。你可以做测试来验证 CSS 是否有效：在 styles.css 里面加上 CSS 样式并观察显示的结果。下面，用你的编辑器打出下面的代码。
```

CSS

```
h1 {
  color: red;
}
```

- 样式化 HTML 元素

  - 我们通过触发元素选择器实现这一点——元素选择器，即直接匹配 HTML 元素的选择器。
 
CSS

```
p {
  color: green;
}
```
 
  - 用逗号将不同选择器隔开，即可一次使用多个选择器。

CSS

```
p,
li {
  color: green;
}
```

- 改变元素的默认行为

只要一个 HTML 文档标记正确，即使像我们的例子那么简单，浏览器都会尽全力将其渲染至可读状态。标题默认使用大号粗体；列表旁总有项目符号。这是因为浏览器自带一个包含默认样式的样式表，默认对任何页面有效。没有了它们，所有文本会夹杂在一起变得一团糟，我们只得从头开始规定，好糟糕。话说回来，所有现代浏览器的默认样式都没什么差距。

不过你可能对浏览器的默认样式不太满意。没关系，只需选定那个元素，加一条 CSS 规则即可。就拿我们的无序列表 <ul>举个例子吧，它自带项目符号，不过要是你跟它有仇，你就可以这样移除它们：

CSS

```
li {
  list-style-type: none;
}
```

[*list-style-type*](https://developer.mozilla.org/zh-CN/docs/Web/CSS/list-style-type)属性示例。

- 使用类名

  - 通过给 HTML 元素加个类名（class），通过不同的类名样式化不同元素。
 
HTML

```
<ul>
  <li>项目一</li>
  <li class="special">项目二</li>
  <li>项目 <em>三</em></li>
</ul>
```

在 CSS 中，要选中这个 special 类，只需在选择器的开头加个西文句点（.）。在你的 CSS 文档里加上如下代码：

CSS

```
.special {
  color: orange;
  font-weight: bold;
}
```

这个 special 类型可不局限于列表，它可以应用到各种元素上。

有时你会发现选择器中，HTML 元素选择器跟类一起出现：

css

```
li.special {
  color: orange;
  font-weight: bold;
}
```

这个意思是说，“选中每个 special 类的 li 元素”。你真要这样，好了，它对 <span> 还有其他元素不起作用了。你可以把这个元素再添上去就是了：

css

```
li.special,
span.special {
  color: orange;
  font-weight: bold;
}
```

- 根据元素在文档中的位置确定样式

有时候，你希望某些内容根据它在文档中的位置而有所不同。这里有很多选择器可以为你提供帮助，但现在我们只介绍几个选择器。在我们的文档中有两个 `<em>`元素——一个在段落内，另一个在列表项内。仅选择嵌套在`<li>` 元素内的`<em>`我们可以使用一个称为包含选择符的选择器，它只是单纯地在两个选择器之间加上一个空格。

将以下规则添加到样式表。

css

```
li em {
  color: rebeccapurple;
}
```

该选择器将选择`<li>`内部的任何`<em>`元素（`<li>`的后代）。因此在示例文档中，你应该发现第三个列表项内的<em>现在是紫色，但是在段落内的那个没发生变化。

另一些可能想尝试的事情是在 HTML 文档中设置直接出现在标题后面并且与标题具有相同层级的段落样式，为此需在两个选择器之间添加一个 + 号 (成为 相邻选择符)

也将这个规则添加到样式表中：

css

```
h1 + p {
  font-size: 200%;
}
```
## CSS 文本样式
## CSS 排版
## 使用 JavaScript 动态编码
## 无障碍
## 为开发人员设计(英语)
## 版本控制
## 扩展模块
## Advanced JavaScript objects
## 客户端 Web API
## 异步 JavaScript
## Web 表单
## 理解客户端工具
## 服务端网站编程
## Web性能
## 测试
## 更多资源及常见问题
## 如何解决常见问题
## 解决常见 CSS 问题
## 使用 HTML 解决常见问题
## 解决 JavaScript 代码的常见问题
## 设计与无障碍
## 工具和安装
## Web 机制
## 关于(英语)
## 面向教育工作者的资源(英语)
## 更新日志

