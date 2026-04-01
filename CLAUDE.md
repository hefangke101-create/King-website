# CLAUDE.md — King Website 项目说明

> 供 Claude 在未来对话中快速恢复项目上下文使用。

---

## 项目概况

- **项目名称**：King-website
- **用途**：King 的个人品牌展示网站，目前为测试效果阶段
- **GitHub 仓库**：https://github.com/hefangke101-create/King-website（Public）
- **线上地址**：https://hefangke101-create.github.io/King-website/（需开启 GitHub Pages）
- **本地路径**：`C:\Users\hefan\Desktop\King-website`
- **技术栈**：纯静态 HTML + CSS + 原生 JS，无框架，无构建工具

---

## 文件夹结构

```
King-website/
├── index.html     # 唯一页面，包含所有内容模块
├── style.css      # 全站样式，含响应式
├── script.js      # 表单交互 + 滚动动画 + 导航阴影
└── CLAUDE.md      # 本文件
```

---

## 页面模块（从上到下）

| 模块 | 锚点 ID | 说明 |
|------|---------|------|
| 导航栏 | — | 固定顶部，logo + 三个锚点链接，滚动后出现阴影 |
| Hero 大标题 | `#home` | 全屏高度，左侧文字 + 右侧装饰圆环 |
| 个人介绍 | `#about` | 左文右图（图片目前为占位符），含3个数据统计 |
| 服务列表 | `#services` | 4张卡片，hover 有上浮阴影效果 |
| 联系方式 | `#contact` | 左侧联系信息 + 右侧联系表单 |
| 页脚 | — | 深色背景，左右各一行文字 |

---

## 设计风格

**选定风格：C — 温暖杂志**
> 米白/奶油色背景，褐色/橙色系点缀，衬线字体，卡片式排版。感觉：亲切、创意、人文。

---

## 色彩系统

所有颜色通过 CSS 变量统一管理（定义在 `style.css` `:root`）：

| 变量名 | 色值 | 用途 |
|--------|------|------|
| `--cream` | `#FAF7F2` | 页面主背景色 |
| `--warm` | `#F2EDE4` | 次背景色（services 区块、输入框背景）|
| `--brown` | `#5C3D2E` | 标题、logo、联系信息文字 |
| `--orange` | `#C8713A` | 主强调色：按钮、section tag、hover、数字 |
| `--dark` | `#2C1A0E` | 最深色，正文标题、页脚背景 |
| `--mid` | `#8A6A52` | 正文段落、次要文字 |
| `--light` | `#BFA98A` | 标签、占位符、分割线 |
| `--white` | `#FFFFFF` | about/contact 区块背景、服务卡片背景 |

---

## 字体系统

| 变量名 | 字体 | 用途 |
|--------|------|------|
| `--serif` | Playfair Display + Noto Serif SC | 所有标题（hero、section title、卡片标题、logo）|
| `--sans` | Noto Sans SC | 正文、段落、表单、导航链接 |

字体来源：Google Fonts（在线加载）

---

## 布局规则

- 最大宽度：`--max: 1100px`，居中对齐
- 圆角：`--radius: 12px`（卡片、输入框）
- 按钮：胶囊形（`border-radius: 50px`）
- About 区块：两栏 grid（`1fr 420px`），图片在右
- Services 区块：`auto-fit minmax(240px, 1fr)`，自动换行
- Contact 区块：两栏等宽 grid（`1fr 1fr`）
- 响应式断点：768px，移动端单栏，导航链接隐藏

---

## 当前内容

### Hero
- 小标签：Personal Brand
- 主标题：让你的 *品牌故事* 被世界看见
- 副标题：策略 · 创意 · 执行 · 结果
- 按钮：开始合作（锚点到 #contact）

### 个人介绍
- 姓名：King
- 数据：50+ 服务客户 / 5年行业经验 / 100% 全力投入
- 图片：目前为占位符（`image-placeholder`），等待真实照片替换

### 服务列表（4项）
1. 品牌定位 — 挖掘核心差异点，建立品牌坐标系
2. 内容战略 — 长期内容规划，持续输出高价值内容
3. 视觉形象 — 配色、字体、排版风格指南
4. 增长咨询 — 数据分析，品牌影响力转化商业机会

### 联系方式
- 邮箱：king@studio.co
- 微信：King_Studio
- 社交媒体：@King的品牌笔记（小红书 / 微博）

---

## 用户偏好

- **不写代码**，所有编码工作由 Claude 完成
- **不需要确认**，Claude 直接动手，完成后告知结果
- 内容暂时为测试用途，不要求完全真实
- 修改后直接 `git add + commit + push`，不需要询问是否推送

---

## Git 信息

- 远程：`origin` → `https://github.com/hefangke101-create/King-website.git`
- 主分支：`main`
- 本地 git user.name：King
- 本地 git user.email：king@king.com（测试用）
