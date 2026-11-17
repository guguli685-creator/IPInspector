# 🌐 GeoPing · IP Inspector

**纯前端 · 零密钥 · 全维度公网 IP 归属与原生属性检测工具**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Pure Frontend](https://img.shields.io/badge/Architecture-Pure%20Frontend-10b981.svg)](#)
[![Zero Token](https://img.shields.io/badge/Security-Zero%20Token%20Exposed-f59e0b.svg)](#)

[在线访问 (GitHub Pages)](https://guguli685-creator.github.io/geoping/) · [功能特性](#-核心功能) · [快速部署](#-部署方式)

</div>

---

## 📖 项目简介

**GeoPing** 是一个基于现代极简设计规范（VitePress + Untitled UI 风格）构建的纯前端网络检测面板。无需任何后端服务器，也无需在代码中硬编码 API Token，可直接托管于 GitHub Pages 或 Cloudflare Pages。

适合在切换 VPN、代理节点或排查跨境网络环境时，快速核验出口 IP 的**地理归属、运营商原生属性（AS Type）、双栈连通性及隐私风控状态**。

---

## ✨ 核心功能

### 1. 🔍 出口识别与任意 IP 检索
- **自动检测与手动查询**：页面加载自动识别本机公网出口；支持在搜索框输入任意 **IPv4 / IPv6** 地址进行归属查询。
- **双栈网络探测**：同步检测当前网络环境的 IPv4 与 IPv6 出口状态。

### 2. 🏷️ 运营商与原生属性研判（AS Type）
- **核心网络类型标注**：自动分析并高亮区分以下网络属性：
  - `ISP` — 原生家庭宽带 / 移动蜂窝运营商
  - `Hosting` — 数据中心 / 云厂商机房节点
  - `Education` — 高校 / 教育科研网络
  - `Business` — 企业商业专线网络
- **完整网络摘要（Summary）**：完整呈现 `ASN 编号`、`Company 所属机构`、`Range (CIDR 网段)`、`Hostname 反向解析`、`Privacy 代理特征`、`Anycast 任播状态` 及 `Abuse contact 投诉邮箱`。

### 3. 🗺️ 无广告实时地图与环境一致性校验
- **嵌入式 Google Maps**：内置纯净无广告的实时交互地图，自动定位至目标 IP 经纬度，支持一键跳转外部完整版地图。
- **时区一致性对比**：自动比对节点所在时区与本地系统时区，提示是否匹配。

### 4. 🎨 现代交互与多端体验
- **双端深度适配**：桌面端采用双栏卡片与四维指标速览布局；移动端自适应单栏折叠与全屏抽屉导航，优化触控体验。
- **多语言与主题切换**：支持 **简体中文 / English / 日本語** 实时切换，内置 **亮色 / 暗色（Dark Mode）** 主题并自动记忆偏好。
- **原始报文查看**：支持一键复制 IP 地址，提供可折叠的 `Raw JSON` 原始聚合接口报文面板。

---

## 🚀 部署方式

本项目为单文件纯前端架构，无任何构建依赖，直接部署即可使用：

1. 将 `index.html` 上传至 GitHub 仓库根目录。
2. 进入仓库的 **Settings** 页面，开启 GitHub Pages：
   ```text
   Settings → Pages → Build and deployment → Deploy from a branch → main → / (root) → Save

 * 等待约 1 分钟部署完成后，即可通过以下地址访问：
   [https://guguli685-creator.github.io/geoping/](https://guguli685-creator.github.io/geoping/)

🛡️ 隐私与数据说明
 * 零密钥安全设计：所有查询均通过浏览器端直接请求 ipinfo.io 公开免密钥接口及公共网络数据源进行聚合补全，不存在任何个人 API Token 泄露风险，可放心用于公开开源仓库。
 * 数据参考性：IP 地理位置、网段划分及运营商分类依赖第三方公开数据库，不同平台的风控库判定可能存在细微差异，检测结果仅作网络环境排查参考。
📄 License
MIT License © guguli685-creator

