# ANGELIC PROTOCOL · 个人作品集

> YAO YIQING · AI Product Manager Portfolio 2026
> 蓝黑赛博风格（Cyberpunk · 赛露露）单页滚动 + 8 章节 iframe 串联

## 目录结构

```
Haruka Yao/
├── index.html                         ← 主页框架（GitHub Pages 入口）
├── README.md                          ← 你正在看的这个
├── pages/                             ← 8 个章节页（被 index.html iframe 引用）
│   ├── cyber-protocol-x07-hero.html       01 首页（Hero + 视频背景）
│   ├── cyber-protocol-profile.html        02 个人档案
│   ├── cyber-protocol-experience.html     03 实习经历
│   ├── cyber-protocol-projects.html       04 实习项目（carousel 横向卡片）
│   ├── personal-projects.html             05 个人项目（4 卡片网格）
│   ├── academic-archive.html              06 学术档案（7 媒资）
│   ├── cyber-protocol-skill-tree.html     07 技能树
│   └── cyber-protocol-contact.html        08 联系方式
└── assets/
    ├── hero.mp4                            首页背景视频（1.5 MB）
    ├── profile-bg.png                      02 个人档案 · 主背景
    ├── image.png                           02 · 装饰图层
    ├── experience-bg.png                   03 实习经历 · 主背景
    ├── skill-tree-bg.webp                  07 技能树 · 主背景
    ├── archive-bg.png                      06 学术档案 · 主背景
    ├── contact-bg.png                      08 联系方式 · 主背景
    ├── projects/                           04-05 项目卡片插图
    │   ├── aipc-1-cover.jpg
    │   ├── mj-erase-bench.jpg
    │   ├── 千问创作者服务平台.png
    │   ├── vivo-AI创作web端.png
    │   ├── vivo-AI相机web端2.png
    │   ├── hero背景图1-2.png
    │   ├── meeting-assistant.png           (05 个人项目)
    │   ├── mini-game-dev.png               (05)
    │   ├── lora-tintin-compare.jpeg        (05)
    │   ├── i2i-manga.png                   (05)
    │   └── personal-projects-bg.png        (05 · 主背景)
    └── archive/                            06 学术档案 · 7 个媒资
        ├── m01-growth-chart.jpg
        ├── m02-ai-video.mp4
        ├── m03-render-board.png
        ├── m04-field-report.png
        ├── m05-strategy-map.png
        ├── m06-sketch-map.png
        └── m07-photo-city-sea.png
```

## 在 GitHub 上部署（GitHub Pages）

### 一次性准备

1. 把整个 `Haruka Yao/` 文件夹上传到 GitHub 仓库根目录：
   ```bash
   cd "D:\Haruka Yao"
   git init
   git add .
   git commit -m "Initial portfolio deployment"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```

2. 仓库名建议用 `<your-username>.github.io` —— 这样默认站点 URL 就是 `https://<your-username>.github.io/`。

### 启用 GitHub Pages

1. 进仓库 `Settings → Pages`
2. **Source**：选 `Deploy from a branch`
3. **Branch**：选 `main`，目录 `/`（root）
4. **Save**

几分钟后（通常 30s-2min）站点上线，URL 会显示在 Pages 设置页顶部。

### 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根加一个 `CNAME` 文件（无后缀），内容是 `yourdomain.com`
2. 在域名 DNS 加 CNAME 记录指向 `<your-username>.github.io`
3. GitHub Pages 设置里勾选 `Enforce HTTPS`

## 本地预览

直接打开 `index.html` 也可以，但**强烈建议用本地 HTTP server**：

```bash
# Python 3
cd "D:\Haruka Yao"
python -m http.server 8000

# Node.js
npx serve .
```

打开 `http://localhost:8000/` 即可看到效果。

> **为什么不直接 file:// 打开**：iframe 加载会受 CORS / same-origin 限制，部分浏览器会拦截；video 自动播放策略在 file:// 下也会更严。HTTP server 不会有这些问题。

## 技术栈

- 纯 HTML + CSS + 原生 JS（**无构建步骤、无框架**）
- GSAP 3.12.5（CDN 引入）—— 章节切换像素消解过渡
- 字体：Google Fonts（Orbitron / JetBrains Mono / Noto Sans SC）
- 没有 npm / 没有 webpack / 没有 React

## 主要交互

| 章节 | 主要交互 |
|---|---|
| 主页 | 8 个章节 iframe 串联 · GSAP 像素消解切换 · 滚动视察背景 · 章节调色 |
| 04 项目 | wheel / 箭头键切换卡片 · 边界不循环（穿透到主页面） |
| 05 个人项目 | 4 卡片网格 · pager 左右翻页 · 不循环 |
| 06 学术档案 | 7 个媒资 · 详情卡片展开 |
| 07 技能树 | 4 大能力方向 · 工具清单 |

## 调试 & 维护

- 修改某个章节页：直接编辑 `pages/xxx.html`，刷新主页即可
- 修改资源：替换同名文件（保留英文文件名）
- 修改章节顺序：在 `index.html` 里改 `SOURCES` 数组和 iframe 的 `data-index`

## 联系

作者：YAO YIQING · 姚怡晴
求职意向：AI 产品经理
学校：华中科技大学