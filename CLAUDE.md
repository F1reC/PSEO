# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目简介

PSEO（Programmatic SEO）项目，为 MeDo（medo.dev）生成 SEO 优化的模板落地页 HTML 片段，嵌入到 Ghost CMS 中作为页面内容展示。

## 核心约束

- **HTML 片段，非完整页面**：产出的 HTML 会被嵌入 Ghost 的 Page 中，Ghost 提供 `<html>`、`<head>`、`<title>`、meta 标签、sitemap 等基础设施
- **不需要 meta 标签**：`description`、`canonical`、`robots`、OG、Twitter Card 等标签在 `<body>` 中无效，必须通过 Ghost 后台 Page Settings 配置
- **JSON-LD 保留在 HTML 中**：`<script type="application/ld+json">` 在 `<body>` 中有效，是模板唯一需要自带的 SEO 元素
- **纯 CSS + HTML，无 JS**：受限于 Ghost HTML Card，只能使用内联 `<style>` + HTML
- **CSS 需要 `!important`**：为了覆盖 Ghost 主题样式，所有 CSS 属性需加 `!important`
- **需要 Ghost Wrapper Reset**：`.kg-html-card,.kg-card,.gh-content .kg-html-card` 的样式重置，防止 Ghost 主题干扰布局

## SEO 规范

### 标题层级
- **不写 `<h1>`**：Ghost 主题会将页面标题渲染为 `<h1>`，模板内容从 `<h2>` 开始
- 层级依次：`<h2>` → `<h3>` → `<h4>`，不跳级

### Ghost 后台需手动配置（每个页面）
1. **Meta title**：如 `AI Study Companion Template | MeDo`
2. **Meta description**：简洁描述，含核心关键词，~150 字符
3. **OG image / Twitter image**：上传产品截图

### 结构化数据
- 使用 `SoftwareApplication` schema（JSON-LD），包含 name、description、category、offers、creator
- 放在 HTML 片段最顶部

### 内链策略
- Related Templates 和 Built with MeDo 链接使用应用广场格式：`https://medo.dev/apps/app-{appId}`
- 不使用 `https://medo.dev/templates/...` 或 `https://app-{id}.appmedo.com` 格式

## 页面结构（当前模板）

```
JSON-LD 结构化数据
<style> 内联 CSS </style>

Hero：badge + h2 标题 + 描述
Features（左右分栏）：
  左侧（垂直居中）：截图 + h3 + 描述 + CTA 按钮 + 信任标签
  右侧：6 张功能卡片（2 列）
Perfect For：h3 + 6 张受众卡片（3 列，白底带边框）
How It Works：h3 + 3 个步骤 + Prompt 推荐框
CTA Box：深色渐变背景 + h3 + CTA 按钮（带 glow 动画）
Related Templates：3 张模板卡片（链接到应用广场）
Built with MeDo：3 张 showcase 卡片（链接到应用广场）
Footer
```

## CSS 设计规范

### 命名空间
- 所有样式在 `.medo-tpl` 下，避免和 Ghost 主题冲突

### 视觉风格
- Apple 风格简洁设计
- 字体：SF Pro Text / 系统字体栈，标题用 Georgia serif
- 品牌蓝：`#0071e3`，文字黑：`#1d1d1f`，次要灰：`#707070`
- 卡片：圆角 20px，hover 上浮 4px + 阴影
- 功能卡片灰底（`#f5f5f7`），受众卡片白底 + 细边框（区分视觉节奏）
- 图标：44px 蓝色背景圆角方块 + 24px 描边图标
- CTA 按钮：渐变蓝 + 14px 圆角矩形（非药丸），CTA Box 中带 glow 动画
- 截图：带 box-shadow 悬浮效果
- Prompt 推荐框：左侧蓝色竖线

### 响应式
- 桌面（>1024px）：左右分栏、3 列卡片
- 平板（769-1024px）：分栏间距缩小、2 列卡片
- 手机（≤768px）：单列堆叠、1 列卡片

### 左右分栏布局
- `grid-template-columns: 2fr 3fr`
- 左侧 `align-items: center` 垂直居中
- 移动端切换为单列

## 文件说明

- `templates.html`：AI Study Companion 模板的最新版本（从 `ai-study-companion-v2.html` 重命名），包含 JSON-LD + 内联 CSS + 完整页面结构

## 开发流程

1. 生成 HTML 模板片段（含 JSON-LD + CSS + HTML 内容）
2. 在 Ghost 编辑器中创建 Page，添加 HTML Card，粘贴片段
3. 在 Ghost Page Settings 中配置 Meta title / description / OG image
4. 发布页面，Ghost 自动收录到 sitemap
