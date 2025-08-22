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

`<link>`语句块里面，我们用属性 rel，让浏览器知道有 CSS 文档存在（所以需要遵守 CSS 样式的规定），并利用属性 href 指定，寻找 CSS 文件的位置。你可以做测试来验证 CSS 是否有效：在 styles.css 里面加上 CSS 样式并观察显示的结果。下面，用你的编辑器打出下面的代码。

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

该选择器将选择`<li>`内部的任何`<em>`元素（`<li>`的后代）。因此在示例文档中，你应该发现第三个列表项内的`<em>`现在是紫色，但是在段落内的那个没发生变化。

另一些可能想尝试的事情是在 HTML 文档中设置直接出现在标题后面并且与标题具有相同层级的段落样式，为此需在两个选择器之间添加一个 + 号 (成为 相邻选择符)

也将这个规则添加到样式表中：

css

```
h1 + p {
  font-size: 200%;
}
```


## CSS 文本样式

- 导引

  - [基本的文本以及字体样式](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Text_styling/Fundamentals)

在本文章中，我们将通篇了解文本、字体样式的所有基础，包括设置字体粗细（font weight）、字体系列及样式（family and style）、字体缩写（font shorthand）、文本排列（text alignment）和其他的效果，还有行（line）以及字符间距（letter spacing）。

  - [样式化](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Text_styling/Styling_lists)

对于大部分内容来说，列表的行为表现跟其他任何文本其实差不多，但你也需要了解还有一些专门用于列表的 CSS 样式以及考虑一些最好的实践方式。本文章将阐释这一切。

  - [样式化链接](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Text_styling/Styling_links)

当你为链接添加样式时，很重要的一点是要去理解怎样有效地使用伪类去修饰链接的状态，以及怎么去修饰不同的接口功能例如导航菜单和面板中所使用的链接。我们将会在这篇文章中讨论这些话题。

  - [网络字体](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Text_styling/Web_fonts)

在这里我们将会详细地探索网络字体——这会允许你与你的网页一同下载自定义字体，来实现更为不同的个性化字体样式。

### 基本文本和字体样式

目标:了解在网页上设计文本所需的基本属性和技术

- CSS中的文字样式设计什么

  - **字体样式:** 作用域字体的属性,会直接应用到文本中,比如使用哪种字体,字体的大小是怎样的,字体是粗体还是斜体,等等.
 
  - **文本布局风格:** 作用于文本的间距以及其他布局功能的属性,比如,允许操行与字之间的空间,以及在内容框中,文本如何对齐.
 
    ***备注:*** 请记住，包含在元素中的文本是作为一个单一的实体。你不能将文字其中一部分选中或添加样式，如果你要这么做，那么你必须要用适合的元素来包装它们，比如 ( `<span>` 或者 `<strong>`), 或者使用伪元素，像::first-letter (选中元素文本的第一个字母), ::first-line (选中元素文本的第一行), 或者 ::selection (当前光标双击选中的文本)

- 字体

HTML

```
<h1>Tommy the cat</h1>

<p>I remember as if it were a meal ago...</p>

<p>
  Said Tommy the Cat as he reeled back to clear whatever foreign matter may have
  nestled its way into his mighty throat. Many a fat alley rat had met its
  demise while staring point blank down the cavernous barrel of this awesome
  prowling machine. Truly a wonder of nature this urban predator — Tommy the cat
  had many a story to tell. But it was a rare occasion such as this that he did.
</p>
```

- 颜色

color 属性设置选中元素的前景内容的颜色 (通常指文本，不过也包含一些其他东西，或者是使用 text-decoration 属性放置在文本下方或上方的线 (underline overline)。

CSS

```
p {
  color: red;
}
```

- 字体种类

要在你的文本上设置一个不同的字体，你可以使用 font-family 属性，这个允许你为浏览器指定一个字体 (或者一个字体的列表)，然后浏览器可以将这种字体应用到选中的元素上。浏览器只会把在当前机器上可用的字体应用到当前正在访问的网站上；如果字体不可用，那么就会用浏览器默认的字体代替 default font.

CSS

```
p {
  font-family: arial;
}
```

- 网页安全字体

说到字体可用性，只有某几个字体通常可以应用到所有系统，因此可以毫无顾忌地使用。这些都是所谓的**网页安全字体**。

|字体名称|泛型|注意|
|:---:|:---:|:---:|
|Arial|sans-serif|通常认为最佳做法还是添加 Helvetica 作为 Arial 的首选替代品，尽管它们的字体面几乎相同，但 Helvetica 被认为具有更好的形状，即使 Arial 更广泛地可用。|
|Courier New|monospace|某些操作系统有一个 Courier New 字体的替代（可能较旧的）版本叫 Courier。使用 Courier New 作为 Courier 的首选替代方案，被认为是最佳做法。|
|Georgia|serif||
|Times New Roman|serif|某些操作系统有一个 Times New Roman 字体的替代（可能较旧的）版本叫 Times。使用 Times 作为 Times New Roman 的首选替代方案，被认为是最佳做法。|
|Trebuchet MS|sans-serif|	你应该小心使用这种字体——它在移动操作系统上并不广泛。|
|Verdana|sans-serif||

***备注:*** 在各种资源中，cssfontstack.com 网站维护了一个可用在 Windows 和 Mac 操作系统上使用的网页安全字体的列表，这可以帮助决策网站的安全性。

***备注:*** 有一个可以下载来自一个网页的自定义字体的方法,允许你通过任何你想要的方法来定制你使用的字体:**网页字体**。

- 默认字体

|名称|定义|示例|
|:---:|:---:|:---:|
|serif|衬线字体，即有衬线的字体（衬线是指字体笔画尾端的小装饰，存在于某些印刷体字体中）。| <span style="font-family: serif;">My big red elephant</span> |
|sans-serif|无衬线字体| <span style="font-family: sans-serif;">My big red elephant</span> |
|monospace|等宽字体，指包含的全部字符的宽度相同的字体，通常在编辑代码时使用。| <span style="font-family: monospace;">My big red elephant</span> |
|cursive|	手写字体，对于英文字符而言通常具有顺滑的连接笔画以模拟手写效果。| <span style="font-family: cursive;">My big red elephant</span> |
|fantasy|		装饰字体。| <span style="font-family: fantasy;">My big red elephant</span> |

- 字体栈

由于你无法保证你想在你的网页上使用的字体的可用性 (甚至一个网络字体可能由于某些原因而出错), 你可以提供一个字体栈 (font stack)，这样的话，浏览器就有多种字体可以选择了。

CSS

```
p {
  font-family: "Trebuchet MS", Verdana, sans-serif;
}
```

***备注:*** 有一些字体名称不止一个单词，比如Trebuchet MS ，那么就需要用引号包裹。

- 字体大小

  - px (像素): 将像素的值赋予给你的文本。这是一个绝对单位，它导致了在任何情况下，页面上的文本所计算出来的像素值都是一样的。
  - em: 1em 等于我们设计的当前元素的父元素上设置的字体大小 (更加具体的话，比如包含在父元素中的大写字母 M 的宽度) 如果你有大量设置了不同字体大小的嵌套元素，这可能会变得棘手，但它是可行的，如下图所示。为什么要使用这个麻烦的单位呢？当你习惯这样做时，那么就会变得很自然，你可以使用em调整任何东西的大小，不只是文本。你可以有一个单位全部都使用 em 的网站，这样维护起来会很简单。
  - rem: 这个单位的效果和 em 差不多，除了 1rem 等于 HTML 中的根元素的字体大小， (i.e. <html>) ，而不是父元素。这可以让你更容易计算字体大小，但是遗憾的是， rem 不支持 Internet Explorer 8 和以下的版本。如果你的项目需要支持较老的浏览器，你可以坚持使用em 或 px, 或者是 polyfill 就像 REM-unit-polyfill. （这个单位在“CSS 的值和单位”一节也有讲解）

元素的 font-size 属性是从该元素的父元素继承的。所以这一切都是从整个文档的根元素——<html>开始，浏览器的 font-size 标准设置的值为 16px

HTML

```
<!-- document base font-size is 16px -->
<article>
  <!-- If my font-size is 1.5em -->
  <p>My paragraph</p>
  <!-- How do I compute to 20px font-size? -->
</article>
```

一个简单的 size 示例

CSS

```
html {
  font-size: 10px;
}

h1 {
  font-size: 2.6rem;
}

p {
  font-size: 1.4rem;
  color: red;
  font-family: Helvetica, Arial, sans-serif;
}
```


- 字体样式、字体粗细、文本转换和文本装饰

  - font-style: 用来打开和关闭文本 italic (斜体)。可能的值如下 (你很少会用到这个属性，除非你因为一些理由想将斜体文字关闭斜体状态)：
 
    - normal: 将文本设置为普通字体 (将存在的斜体关闭)
    - italic: 如果当前字体的斜体版本可用，那么文本设置为斜体版本；如果不可用，那么会利用 oblique 状态来模拟 italics。
    - oblique: 将文本设置为斜体字体的模拟版本，也就是将普通文本倾斜的样式应用到文本中。
 
  - font-weight: 设置文字的粗体大小。这里有很多值可选 (比如 -light, -normal, -bold, -extrabold, -black, 等等), 不过事实上你很少会用到 normal 和 bold以外的值：
 
    - normal, bold: 普通或者加粗的字体粗细
    - lighter, bolder: 将当前元素的粗体设置为比其父元素粗体更细或更粗一步。100–900: 数值粗体值，如果需要，可提供比上述关键字更精细的粒度控制。
 
  - text-transform: 允许你设置要转换的字体。值包括：
 
    - none: 防止任何转型。
    - uppercase: 将所有文本转为大写。
    - lowercase: 将所有文本转为小写。
    - capitalize: 转换所有单词让其首字母大写。
    - full-width: 将所有字形转换成全角，即固定宽度的正方形，类似于等宽字体，允许拉丁字符和亚洲语言字形（如中文，日文，韩文）对齐。
 
  - text-decoration: 设置/取消字体上的文本装饰 (你将主要使用此方法在设置链接时取消设置链接上的默认下划线。) 可用值为：
 
    - none: 取消已经存在的任何文本装饰。
    - underline: 文本下划线。
    - overline: 文本上划线
    - line-through: 穿过文本的线。

你应该注意到 text-decoration 可以一次接受多个值，如果你想要同时添加多个装饰值，比如 text-decoration: underline overline.。同时注意 text-decoration 是一个缩写形式，它由 text-decoration-line, text-decoration-style 和 text-decoration-color 构成。

我们来看一下这几个属性添加到我们的例子中：

CSS

```
html {
  font-size: 10px;
}

h1 {
  font-size: 2.6rem;
  text-transform: capitalize;
}

h1 + p {
  font-weight: bold;
}

p {
  font-size: 1.4rem;
  color: red;
  font-family: Helvetica, Arial, sans-serif;
}
```

 - 文字阴影

你可以为你的文本应用阴影，使用 text-shadow 属性。这最多需要 4 个值，如下例所示：

CSS

```
text-shadow: 4px 4px 5px red;
```

4个属性如下:

1. 阴影与原始文本的水平偏移，可以使用大多数的 CSS 单位 length and size units, 但是 px 是比较合适的。这个值必须指定。
2. 阴影与原始文本的垂直偏移;效果基本上就像水平偏移，除了它向上/向下移动阴影，而不是左/右。这个值必须指定。
3. 模糊半径 - 更高的值意味着阴影分散得更广泛。如果不包含此值，则默认为 0，这意味着没有模糊。可以使用大多数的 CSS 单位 length and size units.
4. 阴影的基础颜色，可以使用大多数的 CSS 颜色单位 CSS color unit. 如果没有指定，默认为 black.

***备注:*** 正偏移值可以向右移动阴影，但也可以使用负偏移值来左右移动阴影，例如 -1px -1px.

 - 多种阴影

你可以通过包含以逗号分隔的多个阴影值，将多个阴影应用于同一文本，例如：

CSS

```
text-shadow:
  -1px -1px 1px #aaa,
  0px 4px 1px rgba(0, 0, 0, 0.5),
  4px 4px 5px rgba(0, 0, 0, 0.7),
  0px 0px 7px rgba(0, 0, 0, 0.4);
```

***备注:*** 你可以看到更多有趣的关于 text-shadow 使用的示例在 Moonlighting with CSS text-shadow.

- 文本布局

有了基本的字体属性，我们来看看我们可以用来影响文本布局的属性。
  
  - 文本对齐

text-align 属性用来控制文本如何和它所在的内容盒子对齐。可用值如下，并且在与常规文字处理器应用程序中的工作方式几乎相同：

    - left:左对齐文本.
    - right:右对齐文本
    - center:居中文字
    - justify:使文本展开，改变单词之间的差距，使所有文本行的宽度相同。你需要仔细使用，它可以看起来很可怕。特别是当应用于其中有很多长单词的段落时。如果你要使用这个，你也应该考虑一起使用别的东西，比如 hyphens，打破一些更长的词语。
  
  - 行高

line-height 属性设置文本每行之间的高，可以接受大多数单位 length and size units，不过也可以设置一个无单位的值，作为乘数，通常这种是比较好的做法。无单位的值乘以 font-size 来获得 line-height。当行与行之间拉开空间，正文文本通常看起来更好更容易阅读。推荐的行高大约是 1.5–2 (双倍间距。) 所以要把我们的文本行高设置为字体高度的 1.5 倍，你可以使用这个：

CSS

```
line-height: 1.5;
```

  - 字母和单词间距

letter-spacing 和 word-spacing 属性允许你设置你的文本中的字母与字母之间的间距、或是单词与单词之间的间距。你不会经常使用它们，但是可能可以通过它们，来获得一个特定的外观，或者让较为密集的文字更加可读。它们可以接受大多数单位 length and size units.

CSS

```
p::first-line {
  letter-spacing: 2px;
  word-spacing: 4px;
}
```

  - 其他属性

    - font 样式:
      - font-variant: 在小型大写字母和普通文本选项之间切换。
      - font-kerning: 开启或关闭字体间距选项。
      - font-feature-settings: 开启或关闭不同的 [OpenType](https://en.wikipedia.org/wiki/OpenType) 字体特性。
      - font-variant-alternates: 控制给定的自定义字体的替代字形的使用。
      - font-variant-caps: 控制大写字母替代字形的使用。
      - font-variant-east-asian: 控制东亚文字替代字形的使用，像日语和汉语。
      - font-variant-ligatures: 控制文本中使用的连写和上下文形式。
      - font-variant-numeric: 控制数字，分式和序标的替代字形的使用。
      - font-variant-position: 控制位于上标或下标处，字号更小的替代字形的使用。
      - font-size-adjust: 独立于字体的实际大小尺寸，调整其可视大小尺寸。
      - font-stretch: 在给定字体的可选拉伸版本中切换。
      - text-underline-position: 指定下划线的排版位置，通过使用 text-decoration-line 属性的underline 值。
      - text-rendering: 尝试执行一些文本渲染优化。
     
    - 文本布局样式：
      -  text-indent: 指定文本内容的第一行前面应该留出多少的水平空间。
      -  text-overflow: 定义如何向用户表示存在被隐藏的溢出内容。
      -  white-space: 定义如何处理元素内部的空白和换行。
      -  word-break: 指定是否能在单词内部换行。
      -  direction: 定义文本的方向 (这取决于语言，并且通常最好让 HTML 来处理这部分，因为它是和文本内容相关联的。)
      -  hyphens: 为支持的语言开启或关闭连字符。
      -  line-break: 对东亚语言采用更强或更弱的换行规则。
      -  text-align-last: 定义一个块或行的最后一行，恰好位于一个强制换行前时，如何对齐。
      -  text-orientation: 定义行内文本的方向。
      -  word-wrap: 指定浏览器是否可以在单词内换行以避免超出范围。
      -  writing-mode: 定义文本行布局为水平还是垂直，以及后继文本流的方向。
     
- Font 简写

许多字体的属性也可以通过 font 的简写方式来设置 . 这些是按照以下顺序来写的： font-style, font-variant, font-weight, font-stretch, font-size, line-height, and font-family.

如果你想要使用 font 的简写形式，在所有这些属性中，只有 font-size 和 font-family 是一定要指定的。

font-size 和 line-height 属性之间必须放一个正斜杠。

CSS

```
font:
  italic normal bold normal 3em/1.5 Helvetica,
  Arial,
  sans-serif;
```
     
### 为列表添加字体样式

- 默认延时的预设值

  - `<ul> 和 <ol> 元素含有 16px（1em）的顶部和底部 margin 和 40px（2.5em）的 padding-left。`
  - `列表项（<li> 元素）默认是没有设置间距的。`
  - `<dl> 元素设置含有 16px（1em）的顶部和底部 margin，但不含内边距。`
  - `<dd> 元素含有 40px（2.5em）的 margin-left。`
  - `在参考中提到的 <p> 元素设置含有 16px（1em）的顶部和底部 margin——与其他的列表类型相同。`
 
- 处理列表间距

CSS

```
/* 通用样式 */

html {
  font-family: Helvetica, Arial, sans-serif;
  font-size: 10px;
}

h2 {
  font-size: 2rem;
}

ul,
ol,
dl,
p {
  font-size: 1.5rem;
}

li,
p {
  line-height: 1.5;
}

/* 描述列表样式 */

dd,
dt {
  line-height: 1.5;
}

dt {
  font-weight: bold;
}
```

- 列表特定样式

   - list-style-type：设置用于列表的项目符号的类型，例如无序列表的方形或圆形项目符号，或有序列表的数字、字母或罗马数字。
   - list-style-position：设置在每个项目开始之前，项目符号是出现在列表项内，还是出现在其外。
   - list-style-image：允许为项目符号使用自定义图片，而不是简单的方形或圆形。
     
  - 符号样式

像上面所提及的，list-style-type 属性允许你设置项目符号的类型，在我们的示例中，我们在有序列表上设置了大写罗马数字：

CSS

```
ol {
  list-style-type: upper-roman;
}
```

  - 项目符号位置

list-style-position 设置在每个项目开始之前，项目符号是出现在列表项内，还是出现在其外。如上所示，默认值为 outside，这使项目符号位于列表项之外。

如果值设置为 inside，项目符号则位于行内。

CSS

```
ol {
  list-style-type: upper-roman;
  list-style-position: inside;
}
```

  - 使用自定义的项目符号图片

list-style-image 属性允许对于项目符号使用自定义图片。其语法相当简单：

CSS

```
ul {
  list-style-image: url(star.svg);
}
```

然而，这个属性在控制项目符号的位置，大小等方面是有限的。最好使用 background 系列属性，你将在背景和边框文章中了解更多信息。在这里我们仅做一点尝试！

在我们的示例中，我们的无序列表最终样式像这样（在之前所见的顶部）：

CSS

```
ul {
  padding-left: 2rem;
  list-style-type: none;
}

ul li {
  padding-left: 2rem;
  background-image: url(star.svg);
  background-position: 0 0;
  background-size: 1.6rem 1.6rem;
  background-repeat: no-repeat;
}
```
  
  - list-style 简写

上述提到的三种属性可以用一个单独的简写属性 list-style 来设置。例如，以下 CSS：

CSS

```
ul {
  list-style-type: square;
  list-style-image: url(example.png);
  list-style-position: inside;
}
```

可以被如下方式代替：

```
ul {
  list-style: square url(example.png) inside;
}
```

- 管理列表计数

  - start

start 属性允许你从 1 以外的数字开始计数。以下示例：

HTML

```
<ol start="4">
  <li>Toast pita, leave to cool, then slice down the edge.</li>
  <li>
    Fry the halloumi in a shallow, non-stick pan, until browned on both sides.
  </li>
  <li>Wash and chop the salad.</li>
  <li>Fill pita with salad, hummus, and fried halloumi.</li>
</ol>
```

  - reversed

reversed 属性将使列表反向计数。以下示例：

HTML

```
<ol start="4" reversed>
  <li>Toast pita, leave to cool, then slice down the edge.</li>
  <li>
    Fry the halloumi in a shallow, non-stick pan, until browned on both sides.
  </li>
  <li>Wash and chop the salad.</li>
  <li>Fill pita with salad, hummus, and fried halloumi.</li>
</ol>
```

***备注:*** 如果反向计数的列表项数比 start 属性的值还要多，计数将继续到零并向负数方向增加。

  - value

value 属性允许设置列表项指定数值，以下示例：

HTML

```
<ol>
  <li value="2">Toast pita, leave to cool, then slice down the edge.</li>
  <li value="4">
    Fry the halloumi in a shallow, non-stick pan, until browned on both sides.
  </li>
  <li value="6">Wash and chop the salad.</li>
  <li value="8">Fill pita with salad, hummus, and fried halloumi.</li>
</ol>
```

  - reversed

reversed 属性将使列表反向计数。以下示例：

HTML

```
<ol start="4" reversed>
  <li>Toast pita, leave to cool, then slice down the edge.</li>
  <li>
    Fry the halloumi in a shallow, non-stick pan, until browned on both sides.
  </li>
  <li>Wash and chop the salad.</li>
  <li>Fill pita with salad, hummus, and fried halloumi.</li>
</ol>
```

***备注:*** 如果反向计数的列表项数比 start 属性的值还要多，计数将继续到零并向负数方向增加。

  - value

HTML


```
<ol>
  <li value="2">Toast pita, leave to cool, then slice down the edge.</li>
  <li value="4">
    Fry the halloumi in a shallow, non-stick pan, until browned on both sides.
  </li>
  <li value="6">Wash and chop the salad.</li>
  <li value="8">Fill pita with salad, hummus, and fried halloumi.</li>
</ol>                 
```

### 样式化链接

**目标:** 学习如何样式应用到链接状态,以及如何使用链接实现常见的 UI 功能,比如导航菜单.

- 链接

在[创建超链接](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/Creating_links)一文中，我们了解了如何根据最佳实践在 HTML 中实现链接。在本文中，我们将以这些知识为基础，向你展示为超链接设计样式的最佳做法。

  - 连接状态

    - Link：有目的地的链接（即不只是一个具名锚点），使用 :link 伪类来应用样式。
    - Visited：已访问过（存在于浏览器历史记录中）的链接，使用 :visited 伪类来应用样式。
    - Hover：被用户鼠标指针悬停的链接，使用 :hover 伪类来应用样式。
    - Focus：被选中的链接（比如通过键盘的 Tab 移动到这个链接，或者使用像 HTMLElement.focus() 这样的方法编程地聚焦链接），使用 :focus 伪类来应用样式。
    - Active：激活（如点击）的链接，使用 :active 伪类来应用样式。

  - 默认样式

    - 链接以下划线表示。
    - 未访问链接为蓝色。
    - 已访问链接为紫色。
    - 悬停链接时，鼠标指针会变成一个小手图标。
    - 聚焦链接的周围有一个轮廓——按下键盘上的制表符键，就能聚焦本页面上的链接。（在 Mac 上，需要使用 option + tab，或通过按下 Ctrl + F7 启用全键盘控制选项。
    - 活动链接为红色。尝试在点击链接时按住鼠标键。
   
HTML

```
<p><a href="#">一个简单的链接</a></p>
```

CSS

```
p {
  font-size: 2rem;
  text-align: center;
}
```

***备注:*** 备注： 本页中的所有链接示例都链接到窗口顶部。空片段（href="#"）用于创建简单示例，并确保每个包含在 <iframe> 中的实时示例不会中断。

  - 可以使用以下 CSS 属性关闭/更改默认样式：
    - color 以改变文字的颜色。
    - cursor 以改变鼠标光标的样式，除非有非常充分的理由，否则不应关闭此功能。
    - outline 以改变文字的轮廓。轮廓有点像边框，唯一的区别是边框占用了盒模型的空间，而轮廓没有；它只是设置在背景图片的顶部。轮廓是一种有用的无障碍辅助工具，因此如果不增加另一种表示重点链接的方法，就不应删除轮廓。
   
  - 将样式应用到一些链接

### Web 字体

**目标:** 学习如何将 web 字体应用到 web 页面,使用第三方服务,或者编写自己的代码.

- 字体种类回顾

正如我们在基本文本和字体样式中所看到的那样，应用到你的 HTML 的字体可以使用 font-family属性来控制。你需要提供一个或多个字体种类名称，浏览器会在列表中搜寻，直到找到它所运行的系统上可用的字体。

CSS

```
p {
  font-family: Helvetica, "Trebuchet MS", Verdana, sans-serif;
}
````

这个系统运行良好，但是对于传统的 web 开发人员来说，字体选择是有限的。只有少数几种字体可以保证兼容所有流行的操作系统——这就是所谓的 Web 安全字体。你可以使用字体堆栈来指定可选择的字体，后面是 Web 安全的替代选项，然后是默认的系统字体，但是为了确保你的设计在每种字体中都显示正常，这样增加了测试的开销。

- Web 字体

首先，在 CSS 的开始处有一个@font-face块，它指定要下载的字体文件：

CSS

```
@font-face {
  font-family: "myFont";
  src: url("myFont.ttf");
}
```

在这个下面，你可以使用 @font-face 中指定的字体种类名称来将你的定制字体应用到你喜欢的任何东西上，比如说：

CSS

```
html {
  font-family: "myFont", "Bitstream Vera Serif", serif;
}
```

关于网页字体有两件重要的事情要记住:

1. 浏览器支持不同的字体格式，因此你需要多种字体格式以获得良好的跨浏览器支持。例如，大多数现代浏览器都支持 WOFF / WOFF2(Web Open Font Format versions 1 and 2，Web 开放字体格式版本 1 和 2)，它是最有效的格式，但是旧版本 IE 只支持 EOT (Embedded Open Type，嵌入式开放类型) 的字体，你可能需要包括一个 SVG 版本的字体支持旧版本的 iPhone 和 Android 浏览器。我们将向你展示如何生成所需的代码。
2. 字体一般都不能自由使用。你必须为他们付费，或者遵循其他许可条件，比如在代码中 (或者在你的站点上) 提供字体创建者。你不应该在没有适当的授权的情况下偷窃字体。

***备注:*** Web 字体作为一种技术从 Internet Explorer 4 开始就得到了的支持！

- 自主学习:web 字体示例

  - 查找字体
 
    - 免费的字体经销商：这是一个可以下载免费字体的网站 (可能还有一些许可条件，比如对字体创建者的信赖)。比如： Font [Squirre](https://www.fontsquirrel.com/)，[dafont](http://www.dafont.com/) 和 [Everything Fonts](https://everythingfonts.com/)。
    - 收费的字体经销商：这是一个收费则字体可用的网站，例如[fonts.com](http://www.fonts.com/)或[myfonts.com](http://www.myfonts.com/)。你也可以直接从字体铸造厂中购买字体，例如[Linotype](https://www.linotype.com/)，[Monotype](http://www.monotype.com/) 或 [Exljbris](http://www.exljbris.com/)。
    - 在线字体服务：这是一个存储和为你提供字体的网站，它使整个过程更容易。更多细节见[使用在线字体服务](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Text_styling/Web_fonts#%E4%BD%BF%E7%94%A8%E5%9C%A8%E7%BA%BF%E5%AD%97%E4%BD%93%E6%9C%8D%E5%8A%A1)。
   
***备注:*** 在右边栏的“查找字体”部分中，你可以单击不同的标记和分类来筛选显示的选项。
   
  - 生成所需代码

    1. 确保你已经满足了任何许可证的要求，如果你打算在一个商业和/或 Web 项目中使用它。
    2. 前往 Fontsquirrel [Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator).
    3. 使用上传字体按钮上传你的两个字体文件。
    4. 勾选复选框，“是的，我上传的字体符合网络嵌入的合法条件。
    5. 点击下载你的套件（kit）。
  
  - 在演示中实现代码

    - 每个字体的多个版本：（比如 .ttf, .woff, .woff2…… 随着浏览器支持需求的改变，提供的字体将随着时间的推移而不断更新。）正如上面提到的，跨浏览器支持需要使用多种字体——这是 Fontsquirrel 的方法，确保你得到了你需要的一切。
    - 每个字体的一个演示 HTML 文件在你的浏览器中加载，看看在不同的使用环境下字体会是什么样子。
    - 一个 stylesheet.css 文件，它包含了你需要的生成好的 @font-face 代码。

- 使用在线字体服务

  1. 前往 [ Google Fonts](https://fonts.google.com/).
  2. 使用左边的过滤器来显示你想要选择的字体类型，并选择一些你喜欢的字体。
  3. 要选择字体种类，按下按钮旁边的 ⊕ 按钮。
  4. 当你选择好字体种类时，按下页面底部的*[Number]* 种类选择。
  5. 在生成的屏幕中，首先需要复制所显示的 HTML 代码行，并将其粘贴到 HTML 文件的头部。将其置于现有的`<link>`元素之上，使得字体是导入的，然后在你的 CSS 中使用它。
  6. 然后，你需要将 CSS 声明复制到你的 CSS 中，以便将自定义字体应用到你的 HTML。

## CSS 排版

### 介绍 CSS 布局

**目标:** 对 CSS 页面布局技术有一个总体的了解.每种技术都能够在后面的教程中获取到更加详细的信息.

**模块中设计关于页面[布局技术](https://developer.mozilla.org/zh-CN/docs/Glossary/Layout_mode)的细节:**

 - 正常布局流

 - display 属性

 - 弹性盒子

 - 网格

 - 浮动

 - 定位

 - CSS 表格布局

 - 多列布局

- 正常布局流

正常布局流（normal flow）是指在不对页面进行任何布局控制时，浏览器默认的 HTML 布局方式

***备注:*** 块元素内容的布局方向被描述为块方向。块方向在英语等具有水平书写模式(writing mode) 的语言中垂直运行。它可以在任何垂直书写模式的语言中水平运行。对应的内联方向是内联内容（如句子）的运行方向。

当你使用 css 创建一个布局时，你正在离开正常布局流，但是对于页面上的多数元素，正常布局流将完全可以创建你所需要的布局。从一个结构良好的 Html 文档开始是非常重要，因为你可以按照默认的方式来搭建页面，而不是自造车轮。

下列布局技术会覆盖默认的布局行为：

 - [display](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display) 属性 — 标准的 value，比如block, inline 或者 inline-block 元素在正常布局流中的表现形式 (见 [Types of CSS boxes](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Box_model#types_of_css_boxes)). 接着是全新的布局方式，通过设置display的值，比如 [CSS Grid](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Grids) 和 [Flexbox](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Flexbox).

 - **浮动**——应用 [float](https://developer.mozilla.org/zh-CN/docs/Web/CSS/float) 值，诸如 left 能够让块级元素互相并排成一行，而不是一个堆叠在另一个上面。

 - [position](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position) 属性 — 允许你精准设置盒子中的盒子的位置，正常布局流中，默认为 static ，使用其他值会引起元素不同的布局方式，例如将元素固定到浏览器视口的左上角。

 - 表格布局— 表格的布局方式可以用在非表格内容上，可以使用display: table和相关属性在非表元素上使用。

 - 多列布局— 这个 [Multi-column layout](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_multicol_layout) 属性可以让块按列布局，比如报纸的内容就是一列一列排布的。

- display 属性

在 css 中实现页面布局的主要方法是设定display属性的值。此属性允许我们更改默认的显示方式。正常流中的所有内容都有一个display的值，用作元素的默认行为方式。例如，英文段落显示在一个段落的下面，这是因为它们的样式是display:block。如果在段落中的某个文本周围创建链接，则该链接将与文本的其余部分保持内联，并且不会打断到新行。这是因为`<a>`元素默认为display:inline。

你可以更改此默认显示行为。例如，`<li>`元素默认为display:block，这意味着在我们的英文文档中，列表项显示为一个在另一个之下。如果我们将显示值更改为inline，它们现在将显示在彼此旁边，就像单词在句子中所做的那样。事实上，你可以更改任何元素的display值，这意味着你可以根据它们的语义选择 html 元素，而不必关心它们的外观。他们的样子是你可以改变的。

除了可以通过将一些内容从block转换为inline（反之亦然）来更改默认表示形式之外，还有一些更大的布局方法以display值开始。但是，在使用这些属性时，通常需要调用其他属性。在讨论布局时，对我们来说最重要的两个值是 display: flex 和 display: grid。

- 弹性盒子

Flexbox 是 CSS 弹性盒子布局模块（[Flexible Box Layout](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_flexible_box_layout) Module）的缩写，它被专门设计出来用于创建横向或是纵向的一维页面布局。要使用 flexbox，你只需要在想要进行 flex 布局的父元素上应用display: flex ，所有直接子元素都将会按照 flex 进行布局。我们来看一个例子。

  - 设置 display:flex

下面这些 HTML 标记描述了一个 class 为wrapper的容器元素，它的内部有三个`<div>`元素。它们在我们的英文文档当中，会默认地作为块元素从上到下进行显示。

现在，当我们把display: flex添加到它的父元素时，这三个元素就自动按列进行排列。这是由于它们变成了flex 项 (flex items)，按照 flex 容器（也就是它们的父元素）的一些 flex 相关的初值进行 flex 布局：它们整整齐齐排成一行，是因为父元素上flex-direction的初值是row。它们全都被拉伸至和最高的元素高度相同，是因为父元素上align-items属性的初值是stretch。这就意味着所有的子元素都会被拉伸到它们的 flex 容器的高度，在这个案例里就是所有 flex 项中最高的一项。所有项目都从容器的开始位置进行排列，排列成一行后，在尾部留下一片空白。

CSS

```
.wrapper {
  display: flex;
}
```

HTML

```
<div class="wrapper">
  <div class="box1">One</div>
  <div class="box2">Two</div>
  <div class="box3">Three</div>
</div>
```

  - 设置 flex 属性

除了上述可以被应用到 flex 容器的属性以外，还有很多属性可以被应用到 flex 项 (flex items) 上面。这些属性可以改变 flex 项在 flex 布局中占用宽/高的方式，允许它们通过伸缩来适应可用空间。

作为一个简单的例子，我们可以在我们的所有子元素上添加flex 属性，并赋值为1，这会使得所有的子元素都伸展并填充容器，而不是在尾部留下空白，如果有更多空间，那么子元素们就会变得更宽，反之，他们就会变得更窄。除此之外，如果你在 HTML 标记中添加了一个新元素，那么它们也会变得更小，来为新元素创造空间——不管怎样，最终它们会调整自己直到占用相同宽度的空间。

CSS

```
.wrapper {
  display: flex;
}

.wrapper {
  flex: 1;
}
```

HTML

```
<div class="wrapper">
  <div class="box1">One</div>
  <div class="box2">Two</div>
  <div class="box3">Three</div>
</div>
```

***备注:*** 为了找到更多关于 Flexbox 的信息,看看我们 [Flexbox](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Flexbox)的文章.

- Grid 布局

同 flex 一样，你可以通过指定 display 的值来转到 grid 布局：display: grid。下面的例子使用了与 flex 例子类似的 HTML 标记，描述了一个容器和若干子元素。除了使用display:grid，我们还分别使用 [grid-template-rows](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows) 和 [grid-template-columns](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns) 两个属性定义了一些行和列的轨道。定义了三个1fr的列，还有两个100px的行之后，无需再在子元素上指定任何规则，它们自动地排列到了我们创建的格子当中。

CSS

```
.wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 100px 100px;
  grid-gap: 10px;
}
```

HTML

```
<div class="wrapper">
  <div class="box1">One</div>
  <div class="box2">Two</div>
  <div class="box3">Three</div>
  <div class="box4">Four</div>
  <div class="box5">Five</div>
  <div class="box6">Six</div>
</div>
```

- 在网格内放置元素

一旦你拥有了一个 grid，你也可以显式地将元素摆放在里面，而不是依赖于浏览器进行自动排列。在下面的第二个例子里，我们定义了一个和上面一样的 grid，但是这一次我们只有三个子元素。我们利用 grid-column 和 grid-row 两个属性来指定每一个子元素应该从哪一行/列开始，并在哪一行/列结束。这就能够让子元素在多个行/列上展开。

CSS

```
.wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 100px 100px;
  grid-gap: 10px;
}

.box1 {
  grid-column: 2 / 4;
  grid-row: 1;
}

.box2 {
  grid-column: 1;
  grid-row: 1 / 3;
}

.box3 {
  grid-row: 2;
  grid-column: 3;
}
```

HTML

```
<div class="wrapper">
  <div class="box1">One</div>
  <div class="box2">Two</div>
  <div class="box3">Three</div>
</div>
```

***备注:*** 这两个例子只是展示了 grid 布局的冰山一角，要深入了解 grid 布局，请参阅我们的文章[Grid Layout](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Grids)。

- 浮动

  - float 属性有四个可能的值:
 
    - left —— 将元素浮动到左侧。
    - right —— 将元素浮动到右侧。
    - none —— 默认值，不浮动。
    - inherit —— 继承父元素的浮动属性。

在下面这个例子当中，我们把一个`<div>`元素浮动到左侧，并且给了他一个右侧的margin，把文字推开。这给了我们文字环绕着这个`<div>`元素的效果，在现代网页设计当中，这是你唯一需要学会的事情。

HTML

```
<h1>Simple float example</h1>

<div class="box">Float</div>

<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla luctus aliquam
  dolor, eu lacinia lorem placerat vulputate. Duis felis orci, pulvinar id metus
  ut, rutrum luctus orci. Cras porttitor imperdiet nunc, at ultricies tellus
  laoreet sit amet. Sed auctor cursus massa at porta. Integer ligula ipsum,
  tristique sit amet orci vel, viverra egestas ligula. Curabitur vehicula tellus
  neque, ac ornare ex malesuada et. In vitae convallis lacus. Aliquam erat
  volutpat. Suspendisse ac imperdiet turpis. Aenean finibus sollicitudin eros
  pharetra congue. Duis ornare egestas augue ut luctus. Proin blandit quam nec
  lacus varius commodo et a urna. Ut id ornare felis, eget fermentum sapien.
</p>
```

CSS

```
.box {
  float: left;
  width: 150px;
  height: 150px;
  margin-right: 30px;
}
```

***备注:*** CSS 浮动的知识会在我们关于 浮动的教程当中被详细地解释。除此之外，如果你想要了解在 Flexbox 和 Grid 布局出现之前我们是如何进行列布局的（仍然有可能碰到这种情形），请阅读我们关于传统布局方式的文章

- 定位技术

定位 (positioning) 能够让我们把一个元素从它原本在正常布局流 (normal flow) 中应该在的位置移动到另一个位置。定位 (positioning) 并不是一种用来给你做主要页面布局的方式，它更像是让你去管理和微调页面中的一个特殊项的位置。

有一些非常有用的技术在特定的布局下依赖于position属性。同时，理解定位 (positioning) 也能够帮助你理解正常布局流 (normal flow)，理解把一个元素移出正常布局流 (normal flow) 是怎么一回事。

有五种主要的定位类型需要我们了解：

  - 静态定位（Static positioning）是每个元素默认的属性——它表示“将元素放在文档布局流的默认位置——没有什么特殊的地方”。
  - 相对定位（Relative positioning）允许我们相对于元素在正常的文档流中的位置移动它——包括将两个元素叠放在页面上。这对于微调和精准设计（design pinpointing）非常有用。
  - 绝对定位（Absolute positioning）将元素完全从页面的正常布局流（normal layout flow）中移出，类似将它单独放在一个图层中。我们可以将元素相对于页面的 <html> 元素边缘固定，或者相对于该元素的最近被定位祖先元素（nearest positioned ancestor element）。绝对定位在创建复杂布局效果时非常有用，例如通过标签显示和隐藏的内容面板或者通过按钮控制滑动到屏幕中的信息面板。
  - 固定定位（Fixed positioning）与绝对定位非常类似，但是它是将一个元素相对浏览器视口固定，而不是相对另外一个元素。这在创建类似在整个页面滚动过程中总是处于屏幕的某个位置的导航菜单时非常有用。
  - 粘性定位（Sticky positioning）是一种新的定位方式，它会让元素先保持和 position: static 一样的定位，当它的相对视口位置（offset from the viewport）达到某一个预设值时，它就会像 position: fixed 一样定位。

 - 简单定位示例

 - 相对定位

 - 绝对定位

 - 固定定位

 - 粘性定位

 - 表格布局

- 多列布局

多列布局模组给了我们 一种把内容按列排序的方式，就像文本在报纸上排列那样。由于在 web 内容里让你的用户在一个列上通过上下滚动来阅读两篇相关的文本是一种非常低效的方式，那么把内容排列成多列可能是一种有用的技术。

要把一个块转变成多列容器 (multicol container)，我们可以使用 [column-count](https://developer.mozilla.org/zh-CN/docs/Web/CSS/column-count)属性来告诉浏览器我们需要多少列，也可以使用[column-width](https://developer.mozilla.org/zh-CN/docs/Web/CSS/column-width)来告诉浏览器以至少某个宽度的尽可能多的列来填充容器。

在下面这个例子中，我们从一个 class 为 container 的`<div>`容器元素里边的一块 HTML 开始。

HTML

```
<div class="container">
  <h1>Multi-column layout</h1>

  <p>Paragraph 1.</p>
  <p>Paragraph 2.</p>
</div>
```

我们指定了该容器的column-width为 200 像素，这让浏览器创建了尽可能多的 200 像素的列来填充这一容器。接着他们共同使用剩余的空间来伸展自己的宽度。

CSS

```
.container {
  column-width: 200px;
}
```

### 浮动

- 什么是 CSS Float (浮动)
  - CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。
  - Float（浮动），往往是用于图像，但它在布局时一样非常有用。
 
- 元素怎样浮动

元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。

一个浮动元素会尽量向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。

浮动元素之后的元素将围绕它。

浮动元素之前的元素将不会受到影响。

- 彼此相邻的浮动元素

如果你把几个浮动的元素放到一起，如果有空间的话，它们将彼此相邻。

- 清楚浮动 - 使用 clear

元素浮动之后，周围的元素会重新排列，为了避免这种情况，使用 clear 属性。

clear 属性指定元素两侧不能出现浮动元素。


### 定位 - CSS Position

- position 属性指定了元素的定位类型.
- position 属性的五个值:
  - static
  - relative
  - fixed
  - absolute
  - sticky
 
元素可以使用的顶部，底部，左侧和右侧属性定位。然而，这些属性无法工作，除非事先设定position属性。他们也有不同的工作方式，这取决于定位方法。

- static 定位

HTML 元素的默认值，即没有定位，遵循正常的文档流对象。

静态定位的元素不会受到 top, bottom, left, right影响。

- fixed 定位

元素的位置相对于浏览器窗口是固定位置。

***注意:*** Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持。

Fixed定位使元素的位置与文档流无关，因此不占据空间。

Fixed定位的元素和其他元素重叠。

- relative

相对定位元素的定位是相对其正常位置。

移动相对定位元素，但它原本所占的空间不会改变。

相对定位元素经常被用来作为绝对定位元素的容器块。

- absolute

绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>

absolute 定位使元素的位置与文档流无关，因此不占据空间。

absolute 定位的元素和其他元素重叠。

- sticky

sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。

position: sticky; 基于用户的滚动位置来定位。

粘性定位的元素是依赖于用户的滚动，在 position:relative 与 position:fixed 定位之间切换。

它的行为就像 position:relative; 而当页面滚动超出目标区域时，它的表现就像 position:fixed;，它会固定在目标位置。

元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。

这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

***注意:*** Internet Explorer, Edge 15 及更早 IE 版本不支持 sticky 定位。 Safari 需要使用 -webkit- prefix (查看以下实例)。

- 重叠元素

元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素

z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）

具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。

***注意:*** 如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。

- 所有 CSS 定位属性

"CSS" 列中的数字表示哪个CSS(CSS1 或者CSS2)版本定义了该属性。

|属性|说明|值|CSS|
|:---:|:---:|:---:|:---:|
|bottom|定义了定位元素下外边距边界与其包含块下边界之间的偏移。|auto<br>length<br>%<br>inherit|2|
|clip|剪辑一个绝对定位的元素|shape<br>auto<br>inherit|2|
|cursor|显示光标移动到指定的类型|url<br>auto<br>crosshair<br>default<br>pointer<br>move<br>e-resize<br>ne-resize<br>nw-resize<br>n-resize<br>se-resize<br>sw-resize<br>s-resize<br>w-resize<br>text<br>wait<br>help|2|
|left|	定义了定位元素左外边距边界与其包含块左边界之间的偏移。|auto<br>length<br>%<br>inherit|2|
|overflow|设置当元素的内容溢出其区域时发生的事情。|auto<br>hidden<br>scroll<br>visible<br>inherit|2|
|overflow-y|指定如何处理顶部/底部边缘的内容溢出元素的内容区域|auto<br>hidden<br>scroll<br>visible<br>no-display<br>no-content|2|
|overflow-x|指定如何处理右边/左边边缘的内容溢出元素的内容区域|auto<br>hidden<br>scroll<br>visible<br>no-display<br>no-content|2|
|position|指定元素的定位类型|absolute<br>fixed<br>relative<br>static<br>inherit|2|
|right|	定义了定位元素右外边距边界与其包含块右边界之间的偏移。|auto<br>length<br>%<br>inherit|2|
|top|	定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。|auto<br>length<br>%<br>inherit|2|
|z-index|设置元素的堆叠顺序|number<br>auto<br>inherit|2|

### 弹性盒子(Flex Box)

弹性盒子是 CSS3 的一种新的布局模式。

CSS3 弹性盒（ Flexible Box 或 flexbox），是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。

引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间。

-弹性盒子内容

弹性盒子由弹性容器(Flex container)和弹性子元素(Flex item)组成。

弹性容器通过设置 display 属性的值为 flex 或 inline-flex将其定义为弹性容器。

弹性容器内包含了一个或多个弹性子元素。

***注意:*** 弹性容器外及弹性子元素内是正常渲染的。弹性盒子只定义了弹性子元素如何在弹性容器内布局。

弹性子元素通常在弹性盒子内一行显示。默认情况每个容器只有一行。

以下元素展示了弹性子元素在一行内显示，从左到右:

```
<!DOCTYPE html>
<html>
<head>
<style>.flex-container {
    display: -webkit-flex;
    display: flex;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
 
.flex-item {
    background-color: cornflowerblue;
    width: 100px;
    height: 100px;
    margin: 10px;
}</style>
</head>
<body>
 
<div class="flex-container">
  <div class="flex-item">flex item 1</div>
  <div class="flex-item">flex item 2</div>
  <div class="flex-item">flex item 3</div> 
</div>
 
</body>
</html>
```

当然我们可以修改排列方式。

如果我们设置 direction 属性为 rtl (right-to-left),弹性子元素的排列方式也会改变，页面布局也跟着改变:

```
body {
    direction: rtl;
}
 
.flex-container {
    display: -webkit-flex;
    display: flex;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
 
.flex-item {
    background-color: cornflowerblue;
    width: 100px;
    height: 100px;
    margin: 10px;
}
```

- flex-direction

flex-direction 属性指定了弹性子元素在父容器中的位置。

 - 语法

    flex-direction: row | row-reverse | column | column-reverse

flex-direction的值有:

 - row：横向从左到右排列（左对齐），默认的排列方式。
 - row-reverse：反转横向排列（右对齐，从后往前排，最后一项排在最前面。
 - column：纵向排列。
 - column-reverse：反转纵向排列，从后往前排，最后一项排在最上面。

- justify-content

内容对齐（justify-content）属性应用在弹性容器上，把弹性项沿着弹性容器的主轴线（main axis）对齐。

justify-content 语法如下：

    justify-content: flex-start | flex-end | center | space-between | space-around

各个值解析:

  - flex-start：
弹性项目向行头紧挨着填充。这个是默认值。第一个弹性项的main-start外边距边线被放置在该行的main-start边线，而后续弹性项依次平齐摆放。

  - flex-end：
弹性项目向行尾紧挨着填充。第一个弹性项的main-end外边距边线被放置在该行的main-end边线，而后续弹性项依次平齐摆放。

  - center：
弹性项目居中紧挨着填充。（如果剩余的自由空间是负的，则弹性项目将在两个方向上同时溢出）。

  - space-between：
弹性项目平均分布在该行上。如果剩余空间为负或者只有一个弹性项，则该值等同于flex-start。否则，第1个弹性项的外边距和行的main-start边线对齐，而最后1个弹性项的外边距和行的main-end边线对齐，然后剩余的弹性项分布在该行上，相邻项目的间隔相等。

  - space-around：
弹性项目平均分布在该行上，两边留有一半的间隔空间。如果剩余空间为负或者只有一个弹性项，则该值等同于center。否则，弹性项目沿该行分布，且彼此间隔相等（比如是20px），同时首尾两边和弹性容器之间留有一半的间隔（1/2*20px=10px）。


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

