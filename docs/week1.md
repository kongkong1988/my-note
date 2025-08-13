# Web3.0入门第一周详细学习任务清单（每天 4 小时）

- 总目标

  - 掌握网页开发基础 + 了解区块链基本概念 + 初步使用钱包与区块链交互
 
## 第一天:前端世界第一步(HTML + CSS)

- 目标:

  - 认识网页组成结构
 
  - 写出第一个网页
 
- 学习内容:

|内容|推荐资源|
|:---:|:---:|
|什么是HTML/CSS|[MDN HTML 入门](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML)&nbsp;&nbsp;[菜鸟教程-HTML](https://www.runoob.com/html/html-tutorial.html)|
|基本标签(`<div>、<p>、<img>`)|同上|
|简单样式(颜色、字体、边框)|[MDN CSS 入门](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)&nbsp;&nbsp;[菜鸟教程-CSS](https://www.runoob.com/css/css-tutorial.html)|

- 练习任务:

  - 做一个【个人介绍页面】:
 
    - 包含标题、图片、段落和你的兴趣爱好
   
## 第二天:JavaScript 入门 + 网页交换

- 目标:

  - 明白 JavaScript 的作用
 
  - 实现按钮点击 → 弹窗
 
- 学习内容:

|内容|推荐资源|
|:---:|:---:|
|JS 变量、函数、实践|B站或 MDN 的 JavaScript入门或者菜鸟教程|
|浏览器控制台|按F12打开 DevTools 看 console.log|
|onclic 事件绑定|B站“原生JS入门”教程|

- 联系任务：

  - 制作一个按钮：点击后弹出“你好，Web3！”
 
  - 学会用 console.log 打印数据
 
  ## 第三天:深入 JavaScript + 数组/对象

  - 目标:
 
    - 掌握 JS 核心语法
   
    - 能处理一组数据
   
  - 学习内容:
 
  |内容|推荐资源|
  |:---:|:---:|
  |数组/对象/条件判断|MDN/廖雪峰JS教程|
  |for / if 等语法|练习中理解|

  - 练习任务:
 
    - 假设你有一个用户钱包地址数组,使用 for 打印所有地址
   
js
```
let wallets = ["0x123", "0xabc", "0xdef"];

```

## 第四天:区块链基本概念入门

- 目标:

  - 明白什么是链、钱包、交易、Gas
 
  - 了解主网和测试网
 
- 学习内容:

|内容|推荐资源|
|:---:|:---:|
|区块链、以太坊、去中心化|看币安学院、知乎、B站【区块链入门】|
|什么是钱包、地址、公私钥|MetaMask  官网/B站|
|什么是 Gas / ETH / 交易Hash|Etherscan|

- 学习任务:

  - 安装 MetaMask 插件
 
  - 连接到**以太坊测试网 Sepolia**
 
  - 在 https://sepoliafaucet.com 领取测试 ETH
 
## 第五天: Remix 部署第一个智能合约

- 目标:

  - 使用 Remix 在线部署第一个合约
 
  -体验链上部署 & 调用

- 学习内容:

|内容|推荐资源|
|:---:|:---:|
|Remix 使用教学|[Remix 教程](https://remix.ethereum.org)|
|河源的编写 / 编译 / 部署流程|B站“*Solidity* + *Remix*”搜索关键词|

- 练习任务：

  - 打开 Remix,部署这个简单的合约:

solidity

```
// HelloWorld.sol
pragma solidity ^0.8.0;

contract HelloWorld {
    string public message = "Hello, Web3!";
}
```

  - 使用 MetaMask 切换测试网签名部署

  - 调用合约查看 message

## 第六天：理解只能合约与前端交互的桥梁（ethers.js）

- 目标：
  - 初步理解什么是 ethers.js
 
  - 学会“钱包连接”操作
 
- 学习内容：

|内容|推荐资源|
|:---:|:---:|
|ethers.j 简介|[ehters.js 文档](https://docs.ethers.org/v6/)|
|浏览器连接钱包代码示例|官方文档 / B站|

- 练习任务:

  - 建立一个 HTML + JS 网页,点击按钮连接 MetaMask:
 
js

```
async function connectWallet() {
  if (window.ethereum) {
    const accounts = await window.ethereum.request({ method: "eth_requestAccounts" });
    console.log("钱包地址：", accounts[0]);
  } else {
    alert("请安装 MetaMask");
  }
}
```

## 第七天：第一周复习 + 项目整合

- 目标：

  - 整合这几天所学
 
  - 做一个【连接钱包 + 显示 ETH 地址 + 输出余额】的小项目
 
- 项目结构：

html

```
- index.html     // 网页结构
- style.css      // 页面样式
- script.js      // JavaScript逻辑
```

js

```
// script.js 示例片段
async function connectAndShowBalance() {
  if (window.ethereum) {
    const provider = new ethers.BrowserProvider(window.ethereum);
    const accounts = await provider.send("eth_requestAccounts", []);
    const balance = await provider.getBalance(accounts[0]);
    alert(`地址：${accounts[0]}\n余额：${ethers.formatEther(balance)} ETH`);
  }
}
```

- 学完这一周，将拥有：

  - 基础网页开发能力
 
  - 区块链核心概念理解
 
  - 能部署只能合约（Remix）
 
  - 能用 JavaScript + ethers.js 连接钱包并显示数据
