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
   
#### 文本格式进阶
#### 创建超链接
#### 挑战:标记信件
#### 挑战:构建网页内容
#### HTML 中的图片
#### 视频和音频内容
#### Mozilla 欢迎页面
#### HTML 表格基础
#### HTML 表格进阶特性和无障碍
#### 挑战:构建行星数据表
#### Forms and buttons(英语)
#### HTML 调试 
### CSS 样式基础
#### CSS 文本样式
#### CSS 排版
#### 使用 JavaScript 动态编码
#### 无障碍
#### 为开发人员设计(英语)
#### 版本控制
## 扩展模块
### Advanced JavaScript objects
### 客户端 Web API
### 异步 JavaScript
### Web 表单
### 理解客户端工具
### 服务端网站编程
### Web性能
### 测试
## 更多资源及常见问题
### 如何解决常见问题
#### 解决常见 CSS 问题
#### 使用 HTML 解决常见问题
#### 解决 JavaScript 代码的常见问题
#### 设计与无障碍
#### 工具和安装
#### Web 机制
### 关于(英语)
### 面向教育工作者的资源(英语)
### 更新日志
