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


## 联系

作者：YAO YIQING · 姚怡晴
求职意向：AI 产品经理
学校：华中科技大学
