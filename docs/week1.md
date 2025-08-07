# ✅ Web3.0入门第一周详细学习任务清单（每天 4 小时）
## 🗓️ 总目标：
让你掌握网页开发基础 + 了解区块链基本概念 + 初步使用钱包与区块链交互

## 📅 [第 1 天：前端世界第一步（HTML + CSS）](./Day1.md)  
- 🎯 目标：
  - 认识网页组成结构
  - 写出第一个网页

### 📘 学习内容：
- 内容	推荐资源
  | --- | --- |
  | 什么是 HTML / CSS	 | [MDN HTML 入门](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content)<br>
  | 基本标签（`<div>、<p>、<img>`）	| 同上
  | 简单样式（颜色、字体、边距）	  | [MDN CSS 入门](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)

### 🛠️ 练习任务：
做一个「个人介绍页面」：
包含标题、图片、段落和你的兴趣爱好

📅 第 2 天：JavaScript 入门 + 网页交互
🎯 目标：
明白 JavaScript 的作用

实现按钮点击 → 弹窗

📘 学习内容：
内容	推荐资源
JS 变量、函数、事件	B站或 MDN 的 JavaScript 入门
浏览器控制台	按 F12 打开 DevTools 看 console.log
onclick 事件绑定	B站 “原生JS入门” 教程

🛠️ 练习任务：
制作一个按钮：点击后弹出“你好，Web3！”

学会用 console.log 打印数据

📅 第 3 天：深入 JavaScript + 数组/对象
🎯 目标：
掌握 JS 核心语法

能处理一组数据

📘 学习内容：
内容	推荐资源
数组 / 对象 / 条件判断	MDN / 廖雪峰 JS教程
for / if 等语法	练习中理解

🛠️ 练习任务：
假设你有一个用户钱包地址数组，使用 for 打印所有地址

js
复制
编辑
let wallets = ["0x123", "0xabc", "0xdef"];
📅 第 4 天：区块链基本概念入门
🎯 目标：
明白什么是链、钱包、交易、Gas

了解主网和测试网

📘 学习内容：
内容	推荐资源
区块链、以太坊、去中心化	看币安学院、知乎、B站「区块链入门」
什么是钱包、地址、公私钥	MetaMask 官网/B站
什么是 Gas / ETH / 交易 Hash	Etherscan

🛠️ 练习任务：
安装 MetaMask 插件

连接到 以太坊测试网 Sepolia

在 https://sepoliafaucet.com 领取测试 ETH

📅 第 5 天：Remix 部署第一个智能合约
🎯 目标：
用 Remix 在线部署第一个合约

体验链上部署 & 调用

📘 学习内容：
内容	推荐资源
Remix 使用教学	Remix 教程
合约编写 / 编译 / 部署流程	B站“Solidity + Remix”搜索关键词

🛠️ 练习任务：
打开 Remix，部署这个简单的合约：

solidity
复制
编辑
// HelloWorld.sol
pragma solidity ^0.8.0;

contract HelloWorld {
    string public message = "Hello, Web3!";
}
使用 MetaMask 切换测试网签名部署

调用合约查看 message

📅 第 6 天：理解智能合约与前端交互的桥梁（ethers.js）
🎯 目标：
初步理解什么是 ethers.js

学会“钱包连接”操作

📘 学习内容：
内容	推荐资源
ethers.js 简介	ethers.js 文档
浏览器连接钱包代码示例	官方文档 / B站

🛠️ 练习任务：
建立一个 HTML + JS 网页，点击按钮连接 MetaMask：

js
复制
编辑
async function connectWallet() {
  if (window.ethereum) {
    const accounts = await window.ethereum.request({ method: "eth_requestAccounts" });
    console.log("钱包地址：", accounts[0]);
  } else {
    alert("请安装 MetaMask");
  }
}
📅 第 7 天：第一周复习 + 项目整合
🎯 目标：
整合这几天所学

做一个「连接钱包 + 显示 ETH 地址 + 输出余额」的小项目

🛠️ 练习项目结构：
html
复制
编辑
- index.html     // 网页结构
- style.css      // 页面样式
- script.js      // JavaScript逻辑
js
复制
编辑
// script.js 示例片段
async function connectAndShowBalance() {
  if (window.ethereum) {
    const provider = new ethers.BrowserProvider(window.ethereum);
    const accounts = await provider.send("eth_requestAccounts", []);
    const balance = await provider.getBalance(accounts[0]);
    alert(`地址：${accounts[0]}\n余额：${ethers.formatEther(balance)} ETH`);
  }
}
🎁 学完这一周，你将拥有：
基础网页开发能力

区块链核心概念理解

能部署智能合约（Remix）

能用 JavaScript + ethers.js 连接钱包并显示数据

如果你需要我：

提供完整项目模板

帮你规划第 2 周路线（开始学 React 和 Solidity）

随时说一句“继续”，我马上接上。
