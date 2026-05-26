# 🌿 草药箱 · 家庭中药管理

一个纯前端的家庭中药材库存与经方管理网页应用：药材入库、经方编辑、一键取药自动扣减库存，数据保存在浏览器本地，无需后端、无需登录、开箱即用。

## ✨ 功能特性

- 🏠 **主页概览**：药材总数、经方总数、使用记录统计 + 最近取药记录
- 🌱 **药材管理**：增删改查、按名称/症状搜索；引用进经方自动标记「可用」，未被引用为「闲置」
- 📖 **经方管理**：动态编辑经方组成（药材 + 克数），自动检测库存是否充足
- ✅ **一键取药**：从经方扣减对应药材的库存克数，自动写入取药记录
- 🔎 **智能匹配**：输入症状关键词，秒级匹配对应药材或经方
- 💾 **本地存储**：所有数据存在浏览器 `localStorage`，刷新不丢失

## 🚀 部署

下面两种方式任选其一，都是 **零配置、零成本、纯静态部署**。

### 方式 A · Vercel（推荐，最快）

1. 把本目录拖到 [vercel.com/new](https://vercel.com/new) 的上传区域
2. 点 **Deploy**，等十几秒
3. 拿到 `https://xxx.vercel.app` 链接，立即可用

或者用 CLI：

```bash
npm i -g vercel
cd 草药箱
vercel        # 首次会让你登录
vercel --prod # 发布到生产环境
```

### 方式 B · GitHub Pages

1. 在 GitHub 新建一个仓库（例如 `caoyaoxiang`），把本目录内所有文件 push 上去
2. 进入仓库 **Settings → Pages**
3. **Source** 选 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`
4. 保存，等 1-2 分钟，访问 `https://<你的用户名>.github.io/caoyaoxiang/`

命令示例：

```bash
cd 草药箱
git init
git add .
git commit -m "init: 草药箱"
git branch -M main
git remote add origin https://github.com/<你的用户名>/caoyaoxiang.git
git push -u origin main
```

### 方式 C · 本地直接打开

双击 `index.html` 即可在浏览器里运行，不依赖任何服务。

## 📁 目录结构

```
草药箱/
├── index.html      # 主应用（单文件，所有 HTML/CSS/JS 都在里面）
├── favicon.svg     # 网页图标
├── vercel.json     # Vercel 部署配置（静态站点）
├── .gitignore      # Git 忽略规则
└── README.md       # 项目说明（本文件）
```

## 🔧 数据相关

- 所有数据保存在浏览器 `localStorage`，key 为 `caoyaoxiang_v1`
- 清空数据：浏览器 DevTools Console 执行 `localStorage.clear()` 后刷新
- 换浏览器/换设备数据**不会**同步，本应用纯本地

## 📜 License

MIT —— 随便用、随便改、随便分享。
