# HTML入门教程
## 入门模块
- 配置环境
  - 安装基础软件
  - 浏览互联网
  - [代码编辑器](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Environment_setup/Code_editors)
    - VS Code
  - 处理文件
    - 网站应该保存在何处
    - 关于大小写和空格的提示
    - 网站应该使用什么结构?  
      1.index.html  
        主页内容  
      2.images 文件夹  
        所有图片  
      3.styles 文件夹  
        为内容提供样式的 *CSS* 代码  
      4.scripts 文件夹  
        所有用于网站添加交互功能的 *JavaScript* 代码  
    - *文件路径(规则)*  
      - 若引用的目标文件与 HTML 文件同级，只需直接使用文件名，例如：my-image.jpg。
      - 要引用子目录中的文件，请在路径前面写上目录名，再加上一个正斜杠。例如：subdirectory/my-image.jpg。
      - 若引用的目标文件位于 HTML 文件的上级，需要加上两个点。举个例子，如果 index.html 在 test-site 的一个子文件夹内，而 my-image.jpg 在 test-site 内，你可以使用 ../my-image.jpg 从 index.html 引用 my-image.jpg。
      - 以上方法可以随意组合，比如：../subdirectory/another-subdirectory/my-image.jpg。   
  - [命令行速成课](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Environment_setup/Command_line)
- [第一个网站](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Your_first_website)
- [Web 标准](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Web_standards)
- [软性技能(英语)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Soft_skills)
## [*核心模块*](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core)
### 使用 HTML 构建内容
#### HTML 基础语法  
前提:安装基础软件,并掌[握处理文件的基本知识](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Environment_setup/Dealing_with_files)  
- 学习成果:
  - HTML 元素的剖析:元素、开始标签、内容、结束标签、属性。
    - HTML 文档由 HTML 元素定义。
    - HTML元素语法
      - HTML 元素以开始标签起始
      - 元素内容
      - HTML 元素以结束标签终止
      - 某些 HTML 元素具有空内容（empty content）
      - [空元素](https://developer.mozilla.org/zh-CN/docs/Glossary/Void_element)在开始标签中进行关闭（以开始标签的结束而结束）
      - 大多数 HTML 元素可拥有属性
    - 嵌套HTML元素
      - 大多数HTML元素可以嵌套(HTML元素可以包含其他HTML元素).
      - HTML文档由相互嵌套的HTML元素构成
    - 元素的属性
      - 属性是HTML元素提供的附加信息.
      - 属性通常出现在HTML标签的开始标签中,用于定义元素的行为、样式、内容或其他特性.
      - 属性总是以 name="value"的形式写在标签内,那么说属性的名称,value是属性的值.
      - 属性值应该始终包括在引号内,常用双引号,不过使用单引号也没有问题.
      - [HTML属性参考手册](https://www.runoob.com/html/html-attributes.html)
      - [HTML标签参考手册](https://www.runoob.com/tags/html-reference.html)
  - HTML body 及其作为页面内容容器的用途
  - 识别[空元素](https://developer.mozilla.org/zh-CN/docs/Glossary/Void_element),以及其与其他元素的区别.
  - 明白为何需要在 HTML 文档顶部声明 doctype。了解历史缘由，但现在它在某种程度上已成为历史遗留。
  - 掌握 HTML 标签正确嵌套的规则

#### "头"里有什么——HTML元信息

html
```
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>我的测试页面</title>
  </head>
  <body>
    <p>这是我的页面</p>
  </body>
</html>
```
- HTML 头部包含HTML`<head>`元素的内容
   - 添加标题`<title>`元素
    title 元素也被以其他的方式使用者,比如在页面添加书签.  
   - 元数据:`<meta>`元素 
    元数据就是描述数据的数据,`<meta>`元素可以被包含进页面的`<head>`元素.
   - 指定文档中的字符编码
    
      html
      ```
      <meta charset="utf-8" />
      ```
#### HTML的标题和段落
- 标题和段落
   - 段落通过`<p>`元素进行定义,标题通过`<h1>`元素进行定义,一共有六种标题元素标签——h1、h2、h3、h4、h5和h6。分别代表不同级别的内容。
   - 实现结构层级
   
html  

```
  <h1>三国演义</h1>

  <p>罗贯中</p>

  <h2>第一回 宴桃园豪杰三结义 斩黄巾英雄首立功</h2>

  <p>
    话说天下大势，分久必合，合久必分。周末七国分争，并入于秦。及秦灭之后，楚、汉分争，又并入于汉……
  </p>

  <h2>第二回 张翼德怒鞭督邮 何国舅谋诛宦竖</h2>

  <p>
    且说董卓字仲颖，陇西临洮人也，官拜河东太守，自来骄傲。当日怠慢了玄德，张飞性发，便欲杀之……
  </p>

  <h3>却说张飞</h3>

  <p>
    却说张飞饮了数杯闷酒，乘马从馆驿前过，见五六十个老人，皆在门前痛哭。飞问其故，众老人答曰：“督邮逼勒县吏，欲害刘公；我等皆来苦告，不得放入，反遭把门人赶打！”……
  </p>
```
     1. 最好只对每个页面使用一次 `<h1>`——这是顶级标题，所有其他标题位于层次结构中的下方。
     2. 请确保在层次结构中以正确的顺序使用标题。不要使用 `<h3>` 来表示副标题，后面再跟 `<h2>` 来表示二级副标题——这是没有意义的，会导致奇怪的结果。
     3. 在现有的六个标题层次中，除非觉得有必要，否则应该争取每页使用不超过三个。有很多层次的文件（例如，深层次的标题层次）会变得笨重，难以浏览。在这种情况下，如果可能的话，建议将内容分散到多个页面。

- 为什么需要结构化
  - 用户在阅读网页时，往往会快速浏览以查找相关内容，经常只是阅读开头的标题（我们通常在一个网页上会花费很少的时间)。如果用户不能在几秒内看到一些有用的内容，他们很可能会感到沮丧并离开。
  - 对网页建立索引的搜索引擎将标题的内容视为影响网页搜索排名的重要关键字。没有标题，你的网页在搜索引擎优化方面效果不佳。
  - 严重视力障碍者通常不会阅读网页；他们用听力来代替。完成这项工作的软件叫做屏幕阅读器。该软件提供了快速访问给定文本内容的方法。在使用的各种技术中，它们通过朗读标题来提供文档的概述，让用户能快速找到他们需要的信息。如果标题不可用，用户将不得不听到整个文档被大声朗读。
  - 使用 CSS 样式化内容，或者使用 JavaScript 做一些有趣的事情，你需要包含相关内容的元素，使得 CSS / JavaScript 可以有效地定位它。

- 为什么我们需要语义
  - 我们需要确保使用了正确的元素来给予内容正确的含义、作用以及外形。

#### 强调与重要性
- 学习成果:
  - 强调和着重强调的含义，以及在 HTML 中应用它们的基本元素，如 `<em>` 和 `<strong>`。
  - 识别根本不应再使用的呈现性标记（例如 `<big>` 和 `<font>`），它们已经被弃用。
  - 识别被重新利用以获得新语义的呈现性标记（例如 `<i>` 和 `<b>`）

html
```
<p>我很<em>庆幸</em>你没有<em>迟到</em>。</p>
```
```
<p>这杯液体<strong>毒性很大</strong>。</p>

<p>就指望你了，千万<strong>不要</strong>迟到！</p>
```
  - 斜体、粗体、下划线......
    - `<i>` 被用来传达传统上用斜体表达的意义：外国文字、分类名称、技术术语、思想……
    - `<b>` 被用来传达传统上用粗体表达的意义：关键字、产品名称、引导句……
    - `<u>` 被用来传达传统上用下划线表达的意义：专有名词、拼写错误……

html
```
<!-- 学名 -->
<p>
  红喉北蜂鸟（学名：<i>Archilocus colubris</i>）是北美东部最常见的蜂鸟品种。
</p>

<!-- 舶来词 -->
<p>
  菜单上有好多舶来词汇，比如 <i lang="uk-latn">vatrushka</i>（东欧乳酪面包）、<i
    lang="id"
    >nasi goreng</i
  >（印尼炒饭）以及 <i lang="fr">soupe à l'oignon</i>（法式洋葱汤）。
</p>

<!-- 已知的错误书写 -->
<p>总有一天我会改掉写<u class="spelling-error">措字</u>的毛病。</p>

<!-- 在定义中，被定义的术语 -->
<dl>
  <dt>语义化 HTML</dt>
  <dd>根据元素的<b>语义</b>意义而不是外观来使用它们。</dd>
</dl>
```

#### 列表    
- 学习成果：
  - 三种类型的列表的 HTML 结构——无序列表、有序列表和描述列表。
  - 每种列表类型的正确使用方法。
  - 列表的更广泛用途，如导航菜单。
- 无序列表
  - 每份无序的清单从 `<ul>` 元素开始，需要包裹清单上所有被列出的项目：
    
html
```
<ul>
  豆浆
  油条
  豆汁
  焦圈
</ul>
```
  - 然后就是用 `<li>`（list item，列表项）元素把每个列出的项目单独包裹起来：

    
html
```
<ul>
  <li>豆浆</li>
  <li>油条</li>
  <li>豆汁</li>
  <li>焦圈</li>
</ul>
```
- 有序列表
  - 有序列表需要按照项目的顺序列出来,除了需要用 `<ol>` 元素而不是 `<ul>` 元素将所有项目包裹：

html
```
<ol>
  <li>沿这条路走到头</li>
  <li>右转</li>
  <li>直行穿过第一个十字路口</li>
  <li>在第三个十字路口处左转</li>
  <li>继续走 300 米，学校就在你的右手边</li>
</ol>
```
- 嵌套列表

html
```
<ol>
  <li>
    先用蛋白一个、盐半茶匙及淀粉两大匙搅拌均匀，调成“腌料”，鸡胸肉切成约一厘米见方的碎丁并用“腌料”搅拌均匀，腌渍半小时。
  </li>
  <li>
    用酱油一大匙、淀粉水一大匙、糖半茶匙、盐四分之一茶匙、白醋一茶匙、蒜末半茶匙调拌均匀，调成“综合调味料”。
  </li>
  <li>
    鸡丁腌好以后，色拉油下锅烧热，先将鸡丁倒入锅内，用大火快炸半分钟，炸到变色之后，捞出来沥干油汁备用。
  </li>
  <li>
    在锅里留下约两大匙油，烧热后将切好的干辣椒下锅，用小火炒香后，再放入花椒粒和葱段一起爆香。随后鸡丁重新下锅，用大火快炒片刻后，再倒入“综合调味料”继续快炒。
    <ul>
      <li>
        如果你采用正宗川菜做法，最后只需加入花生米，炒拌几下就可以起锅了。
      </li>
      <li>如果你在北方，可加入黄瓜丁、胡萝卜丁和花生米，翻炒后起锅。</li>
    </ul>
  </li>
</ol>
``` 
#### 构建文档
- 学习成果:
  - 常用的HTML语义结构元素,如`<main>、<section>、<article>、<header>、<nav>和<footer>,了解如何正确使用他们.
  - 需要在适当的地方使用语义元素,而不是只在需要块级容器的地方使用`<div>`元素,以及这样做的好处(如提高无障碍性).
- 文档的基本组成部分
  - 页眉:`<header>`
  - 导航栏:`<nav>`
  - 主内容:`<main>`.主内容中还可以有各种子内容区段,可用`<article>、<section>和<div>`等元素.
  - 侧边栏:`<aside>`.经常放在`<main>`中.
  - 页脚:`<footer>`.
- 示例代码

  HTML
```
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>我的页面标题</title>
    <link
      href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One"
      rel="stylesheet" />
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <!-- 本站所有网页的统一主标题 -->
    <header>
      <h1>页眉</h1>
    </header>

    <nav>
      <ul>
        <li><a href="#">主页</a></li>
        <li><a href="#">我们的团队</a></li>
        <li><a href="#">项目</a></li>
        <li><a href="#">联系方式</a></li>
      </ul>

      <!-- 搜索栏是站点内导航的一个非线性的方式。 -->

      <form>
        <input type="search" name="q" placeholder="要搜索的内容" />
        <input type="submit" value="搜索" />
      </form>
    </nav>

    <!-- 网页主体内容 -->
    <main>
      <!-- 一篇文章 -->
      <article>
        <h2>文章标题</h2>

        <p>
          但我得向你解释，所有这些谴责快乐和颂扬痛苦的错误观念是如何产生的。为此，我会向你一五一十地说明这一体系，并阐述伟大的真理探索者、人类幸福的杰出建设者的真实教义。
        </p>

        <section>
          <h3>子章节</h3>

          <p>
            没有人因为快乐是快乐而拒绝、厌恶或回避快乐本身，而是因为不知道如何理性地追求快乐的人会遭遇极其痛苦的后果。也没有人因痛苦是痛苦而喜欢或追求或渴望获得痛苦本身，但也偶有辛劳和痛苦能带来极大的快乐的情景。
          </p>

          <p>
            举个微不足道的例子，若不是从中获得好处，我们当中有谁会进行艰苦的体育锻炼？但是，倘若没有恼人的后果，谁有权利指责选择享受快乐的人呢？或者倘若得不到相应快乐，谁能谴责选择避免痛苦的人呢？
          </p>
        </section>

        <section>
          <h3>另外一个子章节</h3>

          <p>
            另一方面，我们以正义的愤慨谴责并厌恶那些被及时行乐迷惑得萎靡不振，被欲望蒙蔽得看不见大难临头的人；因意志软弱而不能履行职责的人，也应受到同样的谴责，这无异于在辛劳和痛苦前退缩。这些情况非常简单且容易区分。闲暇时，当我们的选择权不受限制，当没有什么可以阻止我们做自己最喜欢的事情时，任何快乐都应该受到欢迎，任何痛苦都应该避免。但是在某些情况下，由于责任或商业义务的要求，不时会有不得不拒绝享乐而接受烦恼的情况。
          </p>

          <p>
            因此，智者在这些事情上总是坚持选择的原则：拒绝快乐以获得更大的快乐，或者忍受痛苦以避免更重的痛苦。
          </p>
        </section>
      </article>

      <!-- 辅助内容也可以嵌套在主要内容中 -->
      <aside>
        <h2>相关内容</h2>

        <ul>
          <li><a href="#">哦，我喜欢海边</a></li>
          <li><a href="#">哦，我也喜欢海边</a></li>
          <li><a href="#">尽管在英格兰北部</a></li>
          <li><a href="#">也永远不会停止下雨</a></li>
          <li><a href="#">哦，好吧……</a></li>
        </ul>
      </aside>
    </main>

    <!-- 本站所有网页的统一页脚 -->

    <footer>
      <p>© 2050 某某保留所有权利</p>
    </footer>
  </body>
</html>
```
- HTML布局元素细节[HTML元素参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements)
  - `<main>` 存放本页面独有的内容。每个页面上只能用一次 `<main>`，且直接位于 <body> 中。最好不要把它嵌套进其他元素。
  - `<article>` 包围的内容即一篇文章，与页面其他部分无关（比如一篇博文）。
  - `<section> 与 <article> 类似，但 <section> 更适用于组织页面使其按功能（比如迷你地图、一组文章标题和摘要）分块。一般的最佳用法是：以标题作为开头；也可以把一篇 <article> 分成若干部分并分别置于不同的 <section> 中，也可以把一个区段 <section> 分成若干部分并分别置于不同的 <article> 中，取决于上下文。`
  - `<aside> 包含的内容与主要内容没有直接关系，但可以提供与主要内容间接相关的附加信息（术语条目、作者简介、相关链接，等等）。`
  - `<header> 是简介形式的内容。如果它是 <body> 的子元素，那么就是网站的全局页眉。如果它是 <article> 或<section> 的子元素，那么它是这些部分特有的页眉（此 <header> 非彼标题）。`
  - `<nav> 包含页面主导航功能。其中不应包含二级链接等内容。`
  - `<footer> 包含了页面的页脚部分。`
- 无语义包装器
  - `<span> 是一个行级无语义元素，最好只用于无法找到更好的语义元素来包含内容时，或者不想增加特定的含义时。`
  - `<div> 是一个块级无语义元素，应仅用于找不到更好的块级元素时，或者不想增加特定的意义时。`
- 换行与水平分割线
  - `<br> 可在段落中进行换行；<br> 是唯一能够生成多个短行结构（例如邮寄地址或诗歌）的元素`
  - `<hr> 元素在文档中生成一条水平分割线，表示文本中主题的变化（例如话题或场景的改变）。一般就是一条水平的直线。`

#### 文本格式进阶
- 学习成果:
  - 引用
  - 缩写和首字母缩略图
  - 地址
  - 时间和日期
  - 上标和下标
- 引用: HTML 也有用于标记引用的特性，至于使用哪个元素标记，取决于你引用的是一块还是一行。
  - 块引用:`如果其他地方引用一个块级内容（一个段落、多个段落、一个列表等），你应该把它用 <blockquote> 元素包裹起来表示，并且在 cite 属性里用 URL 来指向引用的资源`
  - 行内引用:`除了使用 <q> 元素以外，行内元素用同样的方式工作。`
  - 引文:cite 属性的内容听起来很有用，但不幸的是，浏览器、屏幕阅读器并没有充分利用它。如果不使用 JavaScript 或 CSS 编写自己的解决方案，就没有办法让浏览器显示 cite 的内容。如果你想在页面上提供引文的来源，你需要在文本中通过链接或其他适当的方式来提供它。

这里有 <cite> 元素，但它是为了包含所引用资源的标题（如书名）。然而，你没有理由不把 <cite> 内的文字以某种方式链接到引用源。  

引文默认的字体样式为斜体。  

- 缩略语:`另一个你在 Web 上看到的相当常见的元素是 <abbr>——它常被用来包裹一个缩略语或缩写，并且提供缩写的解释。当包括这两种情况时，在第一次使用时提供纯文本的完整扩展，同时用 <abbr> 来标记缩写。这为用户代理提供了如何公布/显示内容的提示，同时告知所有用户该缩写的含义.`
- 标记联系方式:`HTML 有个用于标记联系方式的元素——<address>。`
- 上标和下标:`当你使用日期、化学方程式和数学方程式时会偶尔使用上标和下标，以确保它们的正确含义。<sup> 和 <sub> 元素可以解决这样的问题。`
- 展示计算机代码:
  - `<code>：用于标记计算机通用代码。`
  - `<pre>：用于保留空白字符（通常用于代码块）——如果文本中使用了缩进或多余的空白，浏览器将忽略它，你将不会在渲染的页面上看到它。但是，如果你将文本包含在 <pre></pre> 标签中，那么空白将会以与你在文本编辑器中看到的相同的方式渲染出来。`
  - `<var>：用于标记具体变量名。`
  - `<kbd>：用于标记输入电脑的键盘（或其他类型）输入。`
  - `<samp>：用于标记计算机程序的输出。`
- 标记时间和日期
  - `HTML 还支持将时间和日期标记为可供机器识别的格式的 <time> 元素`
#### 创建超链接
- 什么是超链接
  - 超链接是互联网提供的最令人兴奋的创新之一，它们从一开始就一直是互联网的一个特性，使互联网成为互联的网络。超链接使我们能够将我们的文档链接到任何其他文档（或其他资源），也可以链接到文档的指定部分，我们可以在一个简单的网址上提供应用程序。几乎任何网络内容都可以转换为链接，点击（或激活）超链接将使网络浏览器转到另一个网址（URL）。
- 超链接的解析
  - `通过将文本或其他内容包裹在 <a> 元素内，并给它一个包含网址的 href 属性（也称为超文本引用或目标，它将包含一个网址）来创建一个基本链接。`

html
```
<p>
  我创建了一个指向
  <a href="https://www.mozilla.org/zh-CN/">Mozilla 主页</a>的链接。
</p>

```
  - 块级连接
    - 就像之前提到的那样，任何内容，甚至块级元素都可以作为链接出现。

HTML
```
<a href="https://developer.mozilla.org/zh-CN/">
  <h1>MDN Web 文档</h1>
</a>
<p>自从 2005 年起，就开始记载包括 CSS、HTML、JavaScript 等网络技术。</p>
```
  - 使用title属性添加支持信息
    - 你可能要添加到你的链接的另一个属性是 title。这旨在包含关于链接的补充信息，例如页面包含什么样的信息或需要注意的事情。

HTML
```
<p>
  我创建了一个指向
  <a
    href="https://www.mozilla.org/zh-CN/"
    title="了解 Mozilla 使命以及如何参与贡献的最佳站点。">
    Mozilla 主页</a
  >的超链接。
</p>
```
- 统一资源定位符(URL)与路径(path)快速入门
  - 统一资源定位符（Uniform Resource Locator，URL）是一个定义了在网络上的位置的一个文本字符串。
  - URL 使用路径查找文件。路径指定文件系统中你感兴趣的文件所在的位置。
    - 根目录:在根目录，我们有 index.html 和 contacts.html 文件。在真实的网站上，index.html 将会成为我们的主页或着陆页（作为网站或网站特定部分的入口的网页）。
    - 指向当前目录:如果你想在 index.html（顶层 index.html）中包含一个指向 contacts.html 的超链接，你只需要指定想要链接到的文件名。
    - 指向子目录:如果你想在 index.html （顶层 index.html）中包含一个指向 projects/index.html 的超链接，你需要先进入 projects 项目目录，然后通过指定目录的名称，然后是正斜杠，然后是文件的名称指明要链接到的文件 index.html。
    - 指向上级目录:如果你想在 projects/index.html 中包含一个指向 pdfs/project-brief.pdf 的超链接，你必须先返回上级目录，然后再回到 pdfs 目录。
  - 文档片段:超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为文档片段）。要做到这一点，你必须首先给要链接到的元素分配一个 id 属性。
  - 绝对 URL 和相对 URL
    - 绝对URL:指向由其在 Web 上的绝对位置定义的位置，包括协议和域名。像下面的例子，如果 index.html 页面上传到了 projects 这一个目录。并且 projects 目录位于 web 服务站点的根目录，web 站点的域名为 https://www.example.com，那么这个页面就可以通过 https://www.example.com/projects/index.html 访问（或者通过 https://www.example.com/projects/ 来访问，因为在没有指定特定的 URL 的情况下，大多数 web 服务器会默认访问加载 index.html 这类页面）.不管绝对 URL 在哪里使用，它总是指向确定的相同位置。
    - 相对URL:指向与你链接的文件相关的位置，更像我们在前面一节中所看到的位置。例如，如果我们想从示例文件链接 https://www.example.com/projects/index.html 转到相同目录下的一个 PDF 文件，URL 就是文件名（例如 project-brief.pdf），没有其他的信息要求。如果 PDF 文件能够在 projects 的子目录 pdfs 中访问到，相对路径就是 pdfs/project-brief.pdf（对应的绝对 URL 是 https://www.example.com/projects/pdfs/project-brief.pdf）.一个相对的 URL 将指向不同的位置，这取决于引用的文件的实际位置——例如，如果我们把 index.html 文件从 projects 目录移动到 Web 站点的根目录（最高级别，而不是任何目录中），里面的 pdfs/project-brief.pdf 相对 URL 将会指向 https://www.example.com/pdfs/project-brief.pdf，而不是 https://www.example.com/projects/pdfs/project-brief.pdf
      
- 连接最佳实践
  - 使用清晰的连接措辞
    - 使用屏幕阅读器的用户喜欢从页面上的一个链接跳到另一个链接，并且脱离上下文来阅读链接。
    - 搜索引擎使用链接文本来索引目标文件，所以在链接文本中包含关键词是一个很好的主意，以有效地描述与之相关的信息。
    - 读者往往会浏览页面而不是阅读每一个字，他们的眼睛会被页面的特征所吸引，比如链接。他们会找到描述性的链接。
    - 不要重复 URL 作为链接文本的一部分——URL 看起来很丑，当屏幕阅读器一个字母一个字母的读出来的时候听起来就更丑了。
    - 不要在链接文本中说“链接”或“链接到”——它只是无用的内容。屏幕阅读器告诉人们有一个链接。可视化用户也会知道有一个链接，因为链接通常是用不同的颜色设计的，并且存在下划线（这个惯例一般不应该被打破，因为用户习惯了它）。
    - 保持你的链接标签尽可能短——这非常重要，因为屏幕阅读器需要解释整个链接文本。
    - 尽量减少相同文本的多个副本链接到不同地方的情况。如果存在标记为“单击此处”、“单击此处”、“单击此处”这样脱离上下文的链接文本，容易对使用屏幕阅读器的用户带来问题。
  - 链接到非 HTML 资源——留下清晰的指示
    - 当链接到一个需要下载的资源（如 PDF 或 Word 文档）或流媒体（如视频或音频）或有另一个潜在的意想不到的效果（打开一个弹出窗口），你应该添加明确的措辞，以减少混乱

HTML
```
<p>
  <a href="https://www.example.com/large-report.pdf">
    下载销售报告（PDF，大小为 10 MB）
  </a>
</p>

<p>
  <a href="https://www.example.com/video-stream/" target="_blank">
    观看视频（将在新标签页中播放，HD 画质）
  </a>
</p>

```
    - 在下载链接时使用 download 属性  
HTML
```
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=zh-CN"
  download="firefox-latest-64bit-installer.exe">
  下载最新的 Firefox 中文版 - Windows（64 位）
</a>
```
- 电子邮件连接
  - 当点击一个链接或按钮时，可能会开启新的邮件的发送而不是连接到一个资源或页面。这种场景可以使用 <a> 元素和 mailto: URL 协议实现。

HTML
```
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
```
  - 指定详细信息
    - 除了电子邮件地址，你还可以提供其他信息。事实上，任何标准的邮件头字段可以被添加到你提供的 mailto URL 中。其中最常用的是主题（subject）、抄送（cc）和主体（body）（这不是一个真正的标头字段，但允许你为新邮件指定一个简短的内容消息）。每个字段及其值被指定为查询项。

HTML
```
<a
  href="mailto:nowhere@mozilla.org?cc=name2@rapidtables.com&bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email">
  发送含有 cc、bcc、主题和主体的邮件
</a>
```
#### 挑战:标记信件
#### 挑战:构建网页内容
#### HTML 中的图片
- 怎样将图片放在网页上?
  - `要想在网页上放置简单的图像，我们需要使用 <img> 元素。这个元素是空元素（即无法包含任何子内容和结束标签），它需要两个属性才能起作用：src 和 alt。src 属性包含一个 URL，该 URL 指向要嵌入页面的图像。src 属性可以是相对 URL 或绝对 URL，这与 <a> 元素的 href 属性类似。如果没有 src 属性，img 元素就没有图像可加载。`
  - 备选文本
    - 我们接下来要看的属性是 alt。它的值应该是图片的文本描述，用于在图片无法显示或者因为网速慢而加载缓慢的情况下使用。
    - 宽度和高度
      - 你可以用 width 和 height 属性来指定你的图片的宽度和高度。它们的值是不带单位的整数，以像素为单位表示图像的宽度和高度。
    - 图像标题
      - 类似于超链接，你可以通过给图片增加 title 属性来提供更多的信息。
#### 视频和音频内容
- web 中的音频和视频
  - 最早的在线视频和音频的流行得益于专有的基于插件的技术，如 Flash 和 Silverlight。这两种技术存在安全性和无障碍问题，现已过时，取而代之的是原生的 HTML 解决方案，该解决方案包括 <video> 和 <audio> 元素以及用于控制它们的 JavaScript API。在这里，我们不讨论有关 JavaScript 的问题，仅仅讲解有关 HTML 的基础。
  - `<video>` 元素
 
HTML
```
<video src="rabbit320.webm" controls>
  <p>
    你的浏览器不支持 HTML 视频。可点击<a href="rabbit320.mp4">此链接</a>观看。
  </p>
</video>

```
```
值得注意的特性有：

src
同 <img> 元素的使用方式相同，src（来源）属性指向你想要嵌入到网页中的视频资源，它们的运作方式完全相同。

controls
用户应当能够控制视频和音频的播放（这对于患有癫痫的人来说尤为重要）。你必须使用 controls 属性来让视频或音频包含浏览器自带的控制界面，或者使用适当的 JavaScript API 构建自己的界面。至少，界面必须包括启动和停止媒体以及调整音量的方法。

<video> 元素内的段落
这个叫做后备内容，当浏览器不支持 <video> 元素的时候，就会显示这段内容，借此我们能够对旧的浏览器提供回退。你可以添加任何后备内容，在这个例子中我们提供了一个指向这个视频文件的链接，从而使用户至少可以访问到这个文件，而不会局限于浏览器的支持。
```
```
其他特性:

width 和 height
你可以用属性控制视频的尺寸，也可以用 CSS 来控制视频尺寸。无论使用哪种方式，视频都会保持它原始的长宽比——也叫做纵横比。如果你设置的尺寸没有保持视频原始长宽比，那么视频边框将会拉伸，而未被视频内容填充的部分，将会显示默认的背景颜色。

autoplay
这个属性会使音频和视频内容立即播放，即使页面的其他部分还没有加载完全。建议不要在你的网站上自动播放视频（或音频），因为用户可能会反感。

loop
这个属性可以让视频（或者音频）文件在结束时再次开始播放。这个也可能很恼人，同样不建议使用，除非有必要。

muted
这个属性会导致媒体播放时，默认关闭声音。

poster
这个属性指向了一个图像的 URL，这个图像会在视频播放前显示。通常用于粗略的预览或者广告。

preload
这个属性被用来缓冲较大的文件，有三个值可选：

"none"：不缓冲文件
"auto"：页面加载后缓存媒体文件
"metadata"：仅缓冲文件的元数据

```
- `<audio>` 元素
  - `<audio>` 元素与 `<video>` 元素的使用方式几乎完全相同，只有一些细微的差别.

```
<audio> 元素不支持 width/heigth 属性——由于其并没有视觉部件，也就没有内容要设置 width/height。
它同时也不支持 poster 属性——同样，因为没有视觉部件。
```
#### Mozilla 欢迎页面
#### HTML 表格基础
- 什么是表格?
  - 表格是由行和列（表格数据）组成的结构化数据集，它让你快速简单地查找某个表示不同类型数据之间的某种关系的值。
  - 表格是如何工作的?
    - 表格的一个特点就是固定不变。通过在行标题和列标题之间建立视觉关联，信息可以容易地被解读
  - 表格的风格
    - 为了能够让表格在 web 上有效，你需要用 CSS 提供一些样式信息，以及尽可能好的 HTML 固定结构。

- `使用 <th> 元素添加标题`

HTML
```
<table>
  <tr>
    <td>&nbsp;</td>
    <td>诺基</td>
    <td>弗洛尔</td>
    <td>艾拉</td>
    <td>胡安</td>
  </tr>
  <tr>
    <td>品种</td>
    <td>杰克罗斯犬</td>
    <td>贵宾犬</td>
    <td>流浪犬</td>
    <td>可卡犬</td>
  </tr>
  <tr>
    <td>年龄</td>
    <td>16</td>
    <td>9</td>
    <td>10</td>
    <td>5</td>
  </tr>
  <tr>
    <td>主人</td>
    <td>岳母</td>
    <td>我</td>
    <td>我</td>
    <td>嫂子</td>
  </tr>
  <tr>
    <td>饮食习惯</td>
    <td>吃掉所有人的剩菜</td>
    <td>啃咬食物</td>
    <td>吃得多</td>
    <td>吃到爆炸为止</td>
  </tr>
</table>
```

- 允许单元格跨越多行和列

HTML
```
<table>
  <tr>
    <th>动物</th>
  </tr>
  <tr>
    <th>河马</th>
  </tr>
  <tr>
    <th>马</th>
    <td>公马</td>
  </tr>
  <tr>
    <td>母马</td>
  </tr>
  <tr>
    <th>鳄鱼</th>
  </tr>
  <tr>
    <th>鸡</th>
    <td>母鸡</td>
  </tr>
  <tr>
    <td>公鸡</td>
  </tr>
</table>

```
```
让我们使用 colspan 和 rowspan 来改进现有的表格。

首先，把 animals-table.html 和 minimal-table.css 文件复制到你的本地环境，HTML 文件中包含了你刚才看到的动物示例的数据。
接着，使用 colspan 让“动物”、“河马”和“鳄鱼”横跨两列。
最后，使用 rowspan 让“马”和“鸡”竖跨两行。
保存后，用浏览器打开你写的 HTML 文件，看看改进的地方。
```
- 为表格中的列提供共同的样式
  - 不使用 <col> 应用样式
    - `在继续阅读之前，我们将在本文介绍最后一个特性。HTML 有一种为整列数据的定义样式信息的方法：就是 <col> 和 <colgroup> 元素。它们存在是因为如果你想让一列中的每个数据的样式都一样，那么你就要为每个数据都添加一个样式，这样的做法是令人厌烦和低效的。你通常需要在列中的每个 <td> 或 <th> 上定义样式，或者使用一个复杂的选择器，比如 :nth-child()。`
   
HTML
```
<table>
  <tr>
    <th>数据 1</th>
    <th style="background-color: yellow">数据 2</th>
  </tr>
  <tr>
    <td>加尔各答</td>
    <td style="background-color: yellow">橙汁</td>
  </tr>
  <tr>
    <td>机器人</td>
    <td style="background-color: yellow">爵士乐</td>
  </tr>
</table>

```
 - 使用 <col> 应用样式

HTML
```
<table>
  <colgroup>
    <col />
    <col style="background-color: yellow" />
  </colgroup>
  <tr>
    <th>数据 1</th>
    <th>数据 2</th>
  </tr>
  <tr>
    <td>加尔各答</td>
    <td>橙汁</td>
  </tr>
  <tr>
    <td>机器人</td>
    <td>爵士乐</td>
  </tr>
</table>

```

#### HTML 表格进阶特性和无障碍
#### 挑战:构建行星数据表
#### Forms and buttons(英语)
#### [HTML 调试](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/Debugging_HTML) 
