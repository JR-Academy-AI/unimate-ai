# UniMate AI / 牛小匠课代表 — Brand Book

> 这是一个 **UI 规范 / 品牌手册**，不是产品代码。
> 双击 `index.html` 就能看，不需要 npm install / 不需要 build。

---

## 目录结构

```
unimate-ai/
├── index.html              ← 品牌手册（19 sections，双击打开就能看）
├── tokens/
│   ├── tokens.json         ← Design tokens 源数据（Style Dictionary 兼容）
│   └── tokens.css          ← CSS Variables，任何项目 import 即可用
└── assets/mascot/
    ├── default.png         ← 牛小匠主形象
    └── spec-sheet.png      ← 完整 spec 图（设计参考）
```

---

## 怎么用

### 看规范
双击 `index.html`，浏览器打开即可。包含 19 个 section：色彩 / 字体 / Mascot / 按钮 / 输入框 / 标签 / 图标 / 卡片 / 进度 / Alert / Modal / Tooltip / 间距 / 圆角 / 阴影 / 导航 / Dashboard / 文案 / Do & Don't。

### 在产品里用 tokens

```css
/* 任何 CSS 文件顶部 */
@import url('path/to/unimate-ai/tokens/tokens.css');

.my-button {
  background: var(--um-grad-coral);
  border-radius: var(--um-radius-full);
  box-shadow: var(--um-glow-coral);
  padding: 0 var(--um-space-8);
}
```

### 在 JS / Figma / Style Dictionary 里读

`tokens/tokens.json` 是 [W3C Design Tokens 格式](https://design-tokens.github.io/community-group/format/)，可以直接：
- 喂给 [Style Dictionary](https://amzn.github.io/style-dictionary/) 输出 iOS / Android / Tailwind / Sass
- 用 [Tokens Studio for Figma](https://tokens.studio/) 导入到 Figma

---

## 风格 DNA（一句话）

> **Smart but playful** — Duolingo × Brilliant × Linear × Airbotix × 学生 meme。
> 一个会陪你冲 Deadline 的 AI 课代表，不是 SaaS dashboard。

四条不可妥协：**暖白底 (`#FFFEF7`) · 圆胶囊 · IP 驱动 · 克制游戏化**。

---

## 红线（PR 看到立即打回）

- ❌ 主背景用 `#FFFFFF`（必须 `#FFFEF7`）
- ❌ 矩形 / 小圆角按钮、扁平蓝色按钮
- ❌ 蓝色作为品牌主识别色（那是 OpenAI / SaaS 味）
- ❌ 一屏 ≥3 个强渐变 / ≥3 个 sticker / mascot 满屏复读
- ❌ Mascot 状态贴错场景（错误页贴 happy）
- ❌ Caveat 字体进正文 / 标题（只用在短鼓励语）
- ❌ Ant Design / MUI 默认外观未做品牌改造

---

## 待补 (TODO)

- [ ] 设计师交付 8 个差异化 Mascot SVG（happy / studying / thinking / ai-analyzing / charging / tired / deadline / champion）替换占位 PNG
- [ ] 加 Style Dictionary 配置，自动导出 Tailwind preset / iOS Swift / Android XML
- [ ] 等 UniMate AI 产品立项后，把 token 文件软链 / npm 包发布

---

## 维护

源 spec 图：`assets/mascot/spec-sheet.png`（来自 ChatGPT 2026-05-10）
源设计 doc：`~/Downloads/unimate_ai_design_md.md`
最近一次更新：2026-05-11

任何 token 改动必须三处同步：`tokens.json` / `tokens.css` /（如果以后加）`tokens.ts`。
