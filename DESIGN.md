# UniMate AI / 牛小匠课代表 — Design System

> **完整设计规范文档**。目标读者：Claude / 设计师 / 前端 / 内容运营。
> 任何关于「该用什么色、什么字、什么 mascot、什么按钮」的问题，先来这里查。
>
> 配套文件：
> - `index.html` — 视觉设计系统（双击就能看）
> - `tokens/tokens.json` — W3C Design Tokens 源数据
> - `tokens/tokens.css` — `--um-*` CSS 变量
> - `README.md` — 仓库使用说明
>
> Last updated: 2026-05-11 · v0.2

---

## 目录

1. [品牌定位](#1-品牌定位)
2. [品牌 DNA](#2-品牌-dna)
3. [Mascot 系统](#3-mascot-系统)
4. [Color 系统](#4-color-系统)
5. [Typography 系统](#5-typography-系统)
6. [Spacing · Radius · Shadow](#6-spacing--radius--shadow)
7. [Logo & Sticker](#7-logo--sticker)
8. [组件规范](#8-组件规范)
9. [Voice & Tone](#9-voice--tone)
10. [Motion](#10-motion)
11. [Do / Don't 红线](#11-do--dont-红线)
12. [Asset 目录映射](#12-asset-目录映射)
13. [跟 Cert Master 的隔离规则](#13-跟-cert-master-的隔离规则)

---

## 1. 品牌定位

**UniMate AI / 牛小匠课代表** — 大学生（特别是海外华人留学生）的 AI 学业搭子。

| 维度 | 内容 |
|------|------|
| **一句话** | 陪你冲 Deadline 的 AI 课代表 |
| **English** | Your AI Class Rep, hustle through every Deadline. |
| **场景** | Lecture / Tutorial / Assignment / Quiz / Final exam — 大学课程的全周期 AI 陪伴 |
| **目标用户** | 海外华人大学生（澳新加美英），尤其是 IT / 商科 / 工程类 |
| **竞品对标** | Quizlet (背诵卡) · Notion AI (笔记助手) · ChatGPT (通用) · 各校 LMS (官方) |
| **核心差异** | **课代表**人设（不是工具，是同学）+ 错题本 + Deadline 紧迫感 + 牛小匠 IP |
| **母品牌** | JR Academy (匠人学院) — 跟 Cert Master / SigmaQ / JR Jobs 同属一家 |

**不做什么**：
- 不做"代写作业"（违反学术诚信）
- 不做"考试作弊辅助"（同理）
- 不做"代选课"（不替学生做决策）
- 不做纯题库（不抢 Quizlet 的活）

---

## 2. 品牌 DNA

### 一句话
**Smart but playful** — 一只会陪你赶 due 的牛课代表，不是 SaaS dashboard。

### 三圈混合
- **Duolingo 的节奏感** — streak / mascot 表情切换 / 任务 unlock
- **Brilliant 的智识感** — 知识图谱 / 一题一拆解 / 真懂了再过
- **Linear 的现代克制** — 圆角胶囊 / 节制动效 / 无废话 UI
- **Airbotix 的工程审美** — 真东西 / 不堆装饰
- **学生 meme 的烟火气** — "急了急了" / "我裂开了" / "deadline 战神"

### 四条不可妥协（看到就打回）

| 铁律 | Why |
|------|-----|
| **暖白底 `#FFFEF7`** 做大块页面 bg，绝不纯白 `#FFFFFF` | 纯白冷、冰、像 SaaS 后台；暖白才有"教室 / 笔记本"的温度 |
| **圆胶囊**做按钮 / 主要交互 | 矩形硬、扁平蓝按钮 = 加班 SaaS；胶囊圆 = 学生书包扣 |
| **IP 驱动** — 牛小匠贯穿全场景 | 没有 mascot 就丢了灵魂，跟 Notion AI 没区别 |
| **克制游戏化** — 有 streak / 有完课庆祝，但不堆奖牌 | 过度游戏化会变 Duolingo 病态版 |

### 跟其它学习品牌的差别

| 品牌 | 主色 | Mascot | 调性 |
|------|------|--------|------|
| Duolingo | 绿 | 猫头鹰 | 病态游戏化 |
| Quizlet | 紫 | 无 | 工具化、单功能 |
| Notion AI | 黑白 | 无 | 极简专业 |
| Brilliant | 深蓝 | 无 | 硬核智识 |
| Cert Master (姐妹品牌) | 黄 | 企鹅 | 专业 + 备考严肃 |
| **UniMate AI** | **Coral + 多彩** | **牛** | **学生气 + 课代表 + meme 感** |

---

## 3. Mascot 系统

### 3.1 IP 设定

**牛小匠** — 圆胖小公牛。橙黄牛角 / 大眼睛 / 偶尔戴书本 / 偶尔背书包。
单线条 + 平涂色 + 表情夸张（学生表情包风格）。

### 3.2 19 个标准态（禁止自创）

| State | 中文名 | 视觉特征 | 触发场景 | 文件 |
|-------|--------|---------|---------|------|
| `default` | 默认 / 挥手 | 牛小匠 hoodie + 墨镜 + 单手挥手 wave | 默认头像 / 空场景 / 打招呼 / Hero | `assets/mascot/default.png`（=`waving.png`） |
| `happy` | 开心 | 笑眼 + 双手举起 + 庆祝姿势 | 完成任务 / 抽中 / 解锁 | `assets/mascot/happy.png` _(占位中)_ |
| `studying` | 学习中 | 戴眼镜 + 翻书 / 笔记本 | 课程进行中 / 答题中 | `assets/mascot/studying.png` |
| `thinking` | 思考中 | 手托腮 + 头顶问号 | 空状态 / loading / 「想想？」 | `assets/mascot/thinking.png` |
| `ai-analyzing` | AI 分析中 | 戴 AI 眼镜 + 数据屏 + 蓝色玻璃感 | AI 解析 / 出报告 / 智能匹配 | `assets/mascot/ai-analyzing.png` |
| `charging` | 充电中 | 闭眼休息 + 充电符号 + 安详 | 番茄钟休息 / 错题间隔 / pause | `assets/mascot/charging.png` |
| `tired` | 累了 | 黑眼圈 + 颓废 + 坐地上 | 连续刷题过久 / 提醒休息 | `assets/mascot/tired.png` |
| `deadline` | Deadline 战神 | 怒眼 + 火焰 + 冲刺 | due 24h / 紧急 streak | `assets/mascot/deadline.png` |
| `champion` | 满分拿下 | 皇冠 + 金牌 + 100 分 | 满分 / 全通过 / 排行榜首 | `assets/mascot/champion.png` |
| `inspecting` | 调查中 | 单手举放大镜 + 眯眼 + Coral hoodie | **选课情报局** / **学术风险检测** / 作业拆解 / 错题排查 | `assets/mascot/inspecting.png` |
| `scheduling` | 排程 / 课表 | 指日历 + 9 色块 + 大绿勾 + 闪光 | **AI 导入课表成功** / 周计划生成 / DDL 排程 / 课表同步 | `assets/mascot/scheduling.png` |
| `welcome` ⭐ NEW | 欢迎 / 新生入学 | 墨镜 + 白 AI hoodie + 单肩书包 + 挥手 + 闪光 | **第一次启动 / Onboarding hi** / 新学期欢迎页 / 引导教程 | `assets/mascot/welcome.png` |
| `checklist` ⭐ NEW | 任务清单 | 墨镜 + 拿 clipboard + 三红勾 + 铅笔 + 书包 | **DDL 列表** / 今日 To-Do / 任务回顾 / 周报检查 | `assets/mascot/checklist.png` |
| `exploring` ⭐ NEW | 找方向 / 探路 | 墨镜 + 摊地图 + 红色路径 + 头顶 ? | **不知道选什么课** / 路径规划 / 校园找路 / 选专业犹豫 | `assets/mascot/exploring.png` |
| `winner` ⭐ NEW | 冠军全身 | 全身奶牛纹 + 高举奖杯 + 墨镜 | 排行榜 #1 / Bootcamp 毕业 / 期末满分 / 大型成就页 | `assets/mascot/winner.png` |
| `note-taking` ⭐ NEW | 记笔记 | 橙 U hoodie + 张嘴大笑 + 拿小本本 + 铅笔 | **课中记笔记** / 听讲座 / 头脑风暴 / 复习卡 | `assets/mascot/note-taking.png` |
| `notify` ⭐ NEW | 新消息提示 | 探出 Coral 对话气泡 + 红色 "2" 角标 + 眨眼 | **App 通知** / 牛圈新评论 / 私信徽标 / Push 横幅 | `assets/mascot/notify.png` |
| `announce` ⭐ NEW | 公告 / 广播 | 橙 U hoodie + 喊喇叭 + 闪电符号 | **公告横幅** / 新功能上线 / 营销推送 / 活动 banner | `assets/mascot/announce.png` |
| `gpa-up` ⭐ NEW | GPA 提升 | 皇冠 + 墨镜 + 举 "GPA UP↑" 牌 + 满天闪光 | **成绩进步页** / 期末 GPA 上涨 / 学术救援站成功复盘 | `assets/mascot/gpa-up.png` |

### 3.3 选择决策树

```
用户在干嘛？
├── 完成 / 庆祝
│   ├── 普通完成 → happy
│   ├── Quiz 通过 → happy
│   └── 满分 / 100 分 → champion
│
├── 进行中
│   ├── 默认课程进行 → studying
│   ├── AI 在算 / loading → ai-analyzing
│   └── 番茄钟休息 / pause → charging
│
├── 卡住 / 困惑
│   ├── 空状态 / 没动作 → thinking
│   └── 刷太久 / 该休息 → tired
│
├── 紧急 / 倒计时
│   └── due 24h / streak ≥7 天 → deadline
│
├── 调查 / 审查
│   ├── 选课情报局 / 水课榜 / Tutor 评分 → inspecting
│   ├── 学术风险检测 / Turnitin 报告 → inspecting
│   └── 作业拆解 / 错题排查 → inspecting
│
├── 排程 / 课表
│   ├── AI 导入课表成功 → scheduling
│   ├── 周计划生成 / DDL 排程 → scheduling
│   └── 课表同步 / 课节冲突解决 → scheduling
│
├── 第一次见面 / Onboarding ⭐
│   ├── 第一次启动 / 新学期欢迎页 → welcome
│   └── 引导教程 hero → welcome
│
├── 任务清单 / To-Do ⭐
│   ├── DDL 列表 / 今日待办 → checklist
│   ├── 周报 / 任务回顾 → checklist
│   └── 完成度统计页 → checklist
│
├── 不知道选什么 / 找方向 ⭐
│   ├── 选课犹豫 / 选专业犹豫 → exploring
│   ├── 校园找路 / 第一周地图 → exploring
│   └── 路径规划空状态 → exploring
│
├── 重大成就 / 全身款 ⭐
│   ├── 排行榜 #1 / Bootcamp 毕业 → winner
│   └── 期末满分 / 年度报告 hero → winner
│
├── 记笔记 / 听讲 ⭐
│   ├── 课中笔记 / 复习卡 → note-taking
│   └── 头脑风暴 / brainstorm → note-taking
│
├── 通知 / 消息 ⭐
│   ├── App 通知中心 / 牛圈新消息 → notify
│   └── Push 横幅 / 红点徽标 → notify
│
├── 公告 / 广播 ⭐
│   ├── 新功能上线 banner → announce
│   ├── 营销推送 / 活动 hero → announce
│   └── 系统公告横幅 → announce
│
├── GPA / 成绩进步 ⭐
│   ├── 学期 GPA 上涨 → gpa-up
│   └── 学术救援成功复盘 → gpa-up
│
└── 不知道用哪个 → default
```

### 3.4 Mascot 用尺寸 & 工具类

| 尺寸 | 用途 |
|------|------|
| 14-22px | chip 内嵌 / 行内小图标 |
| 32-44px | nav brand / toggle / 进度 tracker |
| 64-128px | 卡片 thumbnail / banner header |
| 200-400px | hero / modal 主形象 / mascot 单元格 |

### 3.5 红线

- ❌ 不要自创新表情（如 "结婚牛 / 喝酒牛"）— 新场景必须 map 到已有 19 态
- ❌ 不要把牛换成其它动物（企鹅是 Cert Master 的）
- ❌ 不要给牛改色（橙黄角不能变蓝，肚皮不能变黑）
- ❌ 不要拉伸 / 压扁 / 倾斜
- ❌ 一屏 ≥3 个不同 mascot（视觉过载）
- ❌ 错误页贴 happy（情绪错配）

---

## 4. Color 系统

### 4.1 品牌色 / Brand (5)

| 名称 | Hex | CSS Var | 角色 |
|------|-----|---------|------|
| Coral | `#FF7A66` | `--um-coral` | **Primary** · CTA · streak |
| Bubblegum | `#FF6BA9` | `--um-bubblegum` | 情绪高点 / 庆祝 / 抽奖 |
| Sunshine | `#FFD43B` | `--um-sunshine` | 高亮 / Pin 标记 / 黄色便利贴 |
| Mint | `#3DD9A9` | `--um-mint` | Success · 通过 · 完成 |
| Purple | `#8B5CF6` | `--um-purple` | AI · 进阶 · 高级功能 |

### 4.2 中性色 / Neutral (7)

| 名称 | Hex | CSS Var | 用途 |
|------|-----|---------|------|
| Ink | `#1F1B2D` | `--um-ink` | 主文字 |
| Ink Soft | `#3D3851` | `--um-ink-soft` | 次正文 |
| Slate | `#6B6478` | `--um-slate` | Caption / 副标 |
| Stone | `#C7C0D5` | `--um-stone` | Disabled / mute |
| Hairline | `#EFE8DA` | `--um-hairline` | Border / divider（暖灰色，不要用普通 #E5E7EB） |
| Canvas | `#FFFEF7` | `--um-canvas` | **页面默认 bg** — 暖白，绝不纯白 |
| White | `#FFFFFF` | `--um-white` | 卡片表面 |

### 4.3 Wash（10% 浅色，chip / alert / card bg）

| 名称 | Hex | CSS Var |
|------|-----|---------|
| Coral wash | `#FFEFE9` | `--um-wash-coral` |
| Bubblegum wash | `#FFEAF3` | `--um-wash-bubblegum` |
| Sunshine wash | `#FFF7D6` | `--um-wash-sunshine` |
| Mint wash | `#DCF6EC` | `--um-wash-mint` |
| Purple wash | `#F1EAFF` | `--um-wash-purple` |

### 4.4 Gradients — first-class（CTA / hero / feature 专用）

UniMate 跟 Cert Master 最大的色彩差异：**渐变是一等公民**。

| 名称 | CSS Var | 配色 |
|------|---------|------|
| Coral grad | `--um-grad-coral` | `linear-gradient(135deg, #FF9A80 0%, #FF5B7E 100%)` |
| Bubblegum grad | `--um-grad-bubblegum` | `linear-gradient(135deg, #FF8FBE 0%, #FF4F8F 100%)` |
| Sunshine grad | `--um-grad-sunshine` | `linear-gradient(135deg, #FFE26B 0%, #FFB638 100%)` |
| Mint grad | `--um-grad-mint` | `linear-gradient(135deg, #6BE7BF 0%, #1FC692 100%)` |
| Purple grad | `--um-grad-purple` | `linear-gradient(135deg, #A78BFA 0%, #7C3AED 100%)` |

**用法**：主 CTA 默认用 `--um-grad-coral`；feature card 上的彩色块用对应色 grad；切勿在同一屏堆 ≥2 种渐变 CTA。

### 4.5 用色决策树

```
要表达什么？
├── 主 CTA / 默认动作 → Coral 实色 OR Coral grad
├── 抽奖 / 庆祝 / 情绪高峰 → Bubblegum
├── 高亮 / Pin / 便利贴标记 → Sunshine
├── 通过 / 完成 / Success → Mint
├── AI / 进阶 / 高级功能 → Purple
├── 中性正文 / 卡片 / 边框 → Neutral 七档
└── chip / alert 浅底 → Wash 五档
```

### 4.6 红线

- ❌ 不要把 Purple 当主 CTA（Purple 是 AI 标识专用）
- ❌ 不要在一屏堆 ≥2 个渐变 CTA（视觉爆炸）
- ❌ 大块页面 bg 不要纯白 `#FFFFFF`（必须暖白 `#FFFEF7`）
- ❌ Border 不要用 `#E5E7EB` 这种冷灰（用 `#EFE8DA` 暖灰 hairline）
- ❌ 不要用 Cert Master 的 `#FFC52A`（那是考证黄，跟 Sunshine 看着像但语义不同）

---

## 5. Typography 系统

### 5.1 字体族

| 角色 | 字体 | CSS Var |
|------|------|---------|
| 主字体 | `'Plus Jakarta Sans', 'PingFang SC', 'HarmonyOS Sans SC', 'Microsoft YaHei', system-ui, ...` | `--um-font-sans` |
| Accent (手写) | `'Caveat', cursive` | `--um-font-accent` |

**Plus Jakarta Sans**：圆润、几何、年轻 — 跟"学生气"匹配；中文 fallback 用 PingFang SC 保证可读。
**Caveat**：仅用于**短鼓励语 / 手写便利贴感装饰**，不要用作正文 / 标题。

### 5.2 字号尺度（10 级，比 Cert Master 大很多）

| Level | Size | Weight | 用途 | CSS Var |
|-------|------|--------|------|---------|
| Hero | 72px | Extrabold (800) | 大 landing / 营销页 | `--um-fs-hero` |
| Page | 48px | Bold (700) | 页面级 H1 | `--um-fs-page` |
| Section | 36px | Bold (700) | 章节大标题 | `--um-fs-section` |
| Card | 20px | Semibold (600) | 卡片标题 | `--um-fs-card` |
| Body Lg | 18px | Regular (400) | 重点正文 | `--um-fs-body-lg` |
| Body | 16px | Regular (400) | 默认正文 | `--um-fs-body` |
| Body Sm | 14px | Regular (400) | 次要正文 | `--um-fs-body-sm` |
| Caption | 12px | Regular (400) | 辅助说明 | `--um-fs-caption` |
| Button | 15px | Bold (700) | 按钮文字 | `--um-fs-button` |
| Eyebrow | 12px | Bold (700) + uppercase | Section 标签 | `--um-fs-eyebrow` |

### 5.3 字重

| 名称 | 值 | CSS Var |
|------|-----|---------|
| Regular | 400 | `--um-fw-regular` |
| Medium | 500 | `--um-fw-medium` |
| Semibold | 600 | `--um-fw-semibold` |
| Bold | 700 | `--um-fw-bold` |
| **Extrabold** | 800 | `--um-fw-extrabold` |

UniMate 比 Cert Master 多一档 **Extrabold (800)** — 用于 Hero / Page 标题，保证学生气的力度感。

### 5.4 行高

| 名称 | 值 | CSS Var |
|------|-----|---------|
| Tight | 1.15 | `--um-lh-tight` |
| Snug | 1.3 | `--um-lh-snug` |
| Normal | 1.5 | `--um-lh-normal` |
| Relaxed | 1.7 | `--um-lh-relaxed` |

### 5.5 红线

- ❌ Caveat 不要用作正文 / 标题（只能用在 ≤10 字的鼓励语 / 装饰）
- ❌ 不要在中文里同时混 ≥2 个 weight（一个层级一个 weight）
- ❌ 不要用 ≥4 种字号在同一屏（视觉过载）
- ❌ Body 字号不要 < 14px（中文阅读不舒服）

---

## 6. Spacing · Radius · Shadow

### 6.1 Spacing — 8pt 网格

```
4 / 8 / 12 / 16 / 24 / 32 / 40 / 48 / 64 / 80
```

| 用途 | 推荐 |
|------|------|
| 内联元素 gap (chip / icon) | 4-8px |
| 表单内 padding | 12-16px |
| 卡片 padding | 16-24px |
| Section 之间 | 32-48px |
| 页面顶/底 padding | 64-80px |

CSS Var：`--um-space-1` ~ `--um-space-20`（数字 = px / 4）。

> ⚠️ 注意：UniMate 用 **8pt 网格**，Cert Master 用 **4pt 网格**。两个项目不要互抄间距值。

### 6.2 Radius — 6 档（含超大 40px）

| 名称 | px | CSS Var | 用途 |
|------|-----|---------|------|
| xs | 4 | `--um-radius-xs` | 小 tag / inline code |
| sm | 8 | `--um-radius-sm` | 输入框 |
| md | 12 | `--um-radius-md` | 小卡片 / chip |
| lg | 24 | `--um-radius-lg` | **卡片默认** |
| xl | 40 | `--um-radius-xl` | **Feature card / hero** |
| full | 9999 | `--um-radius-full` | Pill 按钮 / chip / avatar |

**默认偏好**：所有按钮用 `full` 胶囊；卡片用 `lg` 24px；landing hero block 用 `xl` 40px。
UniMate 偏好"更圆"，所以 `lg` 是 24px（Cert Master 是 16px），有更明显的"学生气"。

### 6.3 Shadow

| 名称 | 值 | 用途 |
|------|-----|------|
| sm | `0 2px 8px rgba(31,27,45,0.06)` | 静态卡片 |
| md | `0 8px 24px rgba(31,27,45,0.08)` | hover 卡片 / 浮起 |
| lg | `0 16px 40px rgba(31,27,45,0.12)` | Modal / floating |
| **glow-coral** | `0 12px 28px rgba(255,122,102,0.32)` | Primary CTA 默认发光 |
| glow-mint | `0 12px 28px rgba(61,217,169,0.28)` | Success / 通过 |
| glow-purple | `0 12px 28px rgba(139,92,246,0.32)` | AI / 高级功能 |
| **shadow-sticker** | `4px 4px 0 rgba(31,27,45,0.95)` | **Sticker 专用 — 硬阴影偏移** |

**shadow-sticker** 是 UniMate 特有：**4px 4px 0** 的硬偏移阴影 — 模拟便利贴 / 印章 / 学生书包扣的物理感。Cert Master 没这个。

---

## 7. Logo & Sticker

### 7.1 Logo 件套（6 件）

| 名称 | 文件 | 用途 |
|------|------|------|
| Horizontal | `assets/logo/horizontal.png` | 官网 header / 邮件签名 / 横向窄区域（彩色版） |
| **Lockup Mono** ⭐ NEW | `assets/logo/lockup-mono.png` | 黑白单色横排：mascot 头像 + 「牛小匠课代表」黑字 — **打印 / 灰底 / 单色场景** |
| Compact | `assets/logo/compact.png` | 海报 / PPT / App 启动屏 |
| Avatar | `assets/logo/avatar.png` | App 图标位 / 头像 / 收藏卡 |
| Fullbody | `assets/logo/fullbody.png` | Hero / banner 大场景 |
| App Icon | `assets/logo/app-icon.png` | 通用 App 图标 |

> **Lockup Mono 使用场景**：印 T-shirt / 贴纸 / 黑白文档头部 / 反白底（深色背景需先反白处理）/ 任何不允许彩色 IP 露出的合作物料。一句话：**有 Coral 配色用 horizontal，没有用 lockup-mono**。

### 7.2 Sticker — 一等公民

UniMate 把 **sticker（贴纸）** 当成品牌资产正式纳入设计系统（Cert Master 没这个）。

| Sticker | 文件 | 用途 |
|---------|------|------|
| Let's Study | `assets/stickers/lets-study.png` | 鼓励 / 启动 CTA / 完课 |

**Sticker 视觉特征**：
- 永远带 `--um-shadow-sticker` 硬偏移阴影 (`4px 4px 0`)
- 永远带白色 outline 边
- 用 Caveat 字体写鼓励语
- 像贴在书本上的便利贴

### 7.3 装饰素材

| 名称 | 文件 | 用途 |
|------|------|------|
| Arrow Curly | `assets/decorations/arrow-curly.png` | 手绘弯箭头 — 指引 / 强调下一步 |

后期补：星星 / 火花 / 圆点等点缀元素，全部用 Caveat 字体调性。

### 7.4 净空规则

Logo 四周必须留出 **≥ 牛头宽度的 1/4** 作为安全边距。

### 7.5 Logo 红线

- ❌ 不要拉伸 / 倾斜 logo
- ❌ 不要改牛角颜色（橙黄是固定的）
- ❌ Sticker 不要去掉硬阴影（去掉就失去物理感）
- ❌ 不要把 logo 当装饰反复重复
- ❌ 一屏 ≥3 个 sticker（视觉爆炸）

---

## 8. 组件规范

### 8.1 Buttons — 圆胶囊 + 渐变 / 实色

UniMate 按钮是**单色块胶囊**（不像 Cert Master 那种双色拼接）。

| 类型 | 背景 | text color |
|------|------|-----------|
| **Primary** | `--um-grad-coral` 渐变 OR `--um-coral` 实色 | 白 |
| **Hover** | 同 Primary + `translateY(-2px)` + 加深 glow | 白 |
| **Secondary** | `--um-white` + 1.5px hairline 描边 | `--um-ink` |
| **Mint CTA** | `--um-grad-mint` | 白 |
| **Purple CTA** | `--um-grad-purple` | 白 |
| **Ghost** | 透明 | `--um-ink-soft` |

- 高度：默认 52px（Cert Master 48px，UniMate 偏大）
- 圆角：`full`
- 字重：Bold (700) - Extrabold (800)
- Glow：Primary / Mint / Purple 必带对应色 glow shadow

### 8.2 Inputs — 4 状态

| 状态 | 边框 | 背景 |
|------|------|------|
| Default | 1.5px `--um-hairline` | `--um-white` |
| Focus | 1.5px `--um-coral` + 4px coral ring (18% alpha) | `--um-white` |
| Filled | 1.5px `--um-hairline` | `--um-canvas` |
| Error | 1.5px `--um-coral` 偏红 | `--um-wash-coral` |

- 字号：16px (避免 iOS 自动放大)
- 圆角：`sm` (8px)
- padding：`12px 16px`
- Textarea 计数器在右下角，`position: absolute`，加白色渐变蒙层避免文字重叠

### 8.3 Cards — 圆角卡片 + 彩色 wash 头

| 元素 | 规则 |
|------|------|
| 圆角 | `lg` (24px)，feature card 用 `xl` (40px) |
| Padding | 16-24px |
| Shadow | sm 默认 / md hover |
| 头图区 | 用 wash 色 + mascot 插图 / 渐变 |
| 标题 | Card 字号 (20px) + Semibold |

### 8.4 Chips & Tags

| 类型 | 样式 |
|------|------|
| Coral chip | `--um-wash-coral` 底 + coral 文字 |
| Mint chip | `--um-wash-mint` 底 + mint 文字 |
| Sunshine chip | `--um-wash-sunshine` 底 + 深棕文字 |
| Outline | 白底 + hairline 描边 |

### 8.5 Toggle / Check / Radio

| 组件 | 关闭态 | 开启态 |
|------|--------|--------|
| Toggle | `--um-stone` 底 + 白 knob | `--um-coral` 底 + 白 knob 含小牛头 |
| Checkbox | 白底 + 2px hairline | `--um-coral` 底 + 白 ✓ |
| Radio | 白底 + 2px hairline | 2px coral 边 + coral 实心圆 |

### 8.6 Alerts

| 类型 | bg | icon-wrap |
|------|-----|-----------|
| Success | `--um-wash-mint` | mint 圆 + 白 ✓ |
| Warning | `--um-wash-sunshine` | sunshine 圆 + 黑 ! |
| Danger | `--um-wash-coral` | coral 圆 + 白 × |
| Info | `--um-wash-purple` | purple 圆 + 白 i |

### 8.7 Progress — 糖果条纹

```css
background:
  repeating-linear-gradient(-45deg, rgba(255,255,255,0.22) 0 8px, transparent 8px 16px),
  var(--um-grad-coral);
animation: stripe-march 1.6s linear infinite;
```

进度条上方浮 40px tracker，里面装小牛头。

### 8.8 Modal / Tooltip / Pagination

详见 `index.html` 对应 section。

---

## 9. Voice & Tone

### 9.1 整体调性

**像同班课代表** — 比你更卷一点，会催作业但用 meme 催，紧迫感拉满但不冷漠。

### 9.2 文案规则

| ✅ 这样写 | ❌ 不要这样 |
|----------|-----------|
| due 还有 18h，启动！ | 距离截止时间还有 18 小时 |
| 还差 2 个 quiz 就满分了 | 还有 2 个测验未完成 |
| 我裂开了，再做 5 道 | 您当前正确率较低 |
| Coffee 时间 ☕ 别忘了喝水 | 请注意休息 |
| 牛小匠帮你拆了这题 | 系统已为您解析 |

### 9.3 永远别用

- "您" — 用"你"
- "亲爱的同学" — 太教务系统
- "强烈推荐" — 营销废话
- "智能化 / 数字化 / 赋能" — 政府报告味
- "宝子 / 家人们" — 太抖音

### 9.4 学生 meme 用词清单（可用）

- "急了急了"
- "我裂开了"
- "Deadline 战神"
- "求生欲拉满"
- "卷不动了"
- "今晚通宵？"
- "GG / 寄"
- "稳了 / 拿下"

⚠️ 用 meme 要适度，一屏 ≤2 个，不然变低龄。

### 9.5 不同场景的语气

| 场景 | 范例 |
|------|------|
| 默认引导 | "开始今天的 Lecture" |
| 完成奖励 | "拿下！+30 经验" |
| Quiz 通过 | "稳了！本章 95% 正确率" |
| Deadline 提醒 | "Assignment 还有 18h，启动！" |
| 错题 | "这题我也卡了好久 — 再拆一次？" |
| 累了 | "刷了 2h 了 ☕ 喝口水歇 5 分钟？" |
| 报错 | "网炸了，点这里重试" |
| 满分 | "100 分！截图发朋友圈？" |

---

## 10. Motion

### 10.1 Duration

| 名称 | 值 | 用途 |
|------|-----|------|
| press | 120ms | 按钮按下 |
| hover | 180ms | hover 过渡 |
| card | 200ms | 卡片浮起 |
| modal | 260ms | 弹窗进出 |
| mascot | 400ms | mascot 表情切换 |
| **blob** | 7s | 背景渐变 blob 缓动 |

### 10.2 Easing

| 名称 | 值 | 用途 |
|------|-----|------|
| standard | `cubic-bezier(0.2, 0.8, 0.2, 1)` | 默认所有缓动 |
| spring | `cubic-bezier(0.34, 1.56, 0.64, 1)` | 弹跳（mascot 入场 / champion 庆祝） |

### 10.3 关键动效

- **按钮 hover**：`translateY(-2px)` + 加深 glow
- **卡片 hover**：`translateY(-3px)` + shadow sm → md
- **进度条**：糖果条纹 1.6s linear infinite
- **Mascot 入场**：spring easing + scale (0.8 → 1)
- **Sticker 入场**：spring easing + 旋转 -5° → 0°（像贴上去的便利贴）
- **Background blob**：7s 慢速色彩呼吸（landing 页用）

### 10.4 红线

- ❌ 不要 ≥1s 的核心动画（用户没耐心，blob 例外）
- ❌ 不要让 mascot 持续抖 / 转
- ❌ 不要给 Body 文字加 fade-in 动画（影响阅读）

---

## 11. Do / Don't 红线

### 11.1 视觉

| ✅ Do | ❌ Don't |
|-------|---------|
| 页面 bg = `--um-canvas` (#FFFEF7)，卡片 = 白 | 页面 bg = `#FFFFFF` |
| 主 CTA = Coral grad / 实色胶囊 | 紫色 / 蓝色矩形按钮 |
| Mascot 用 9 标准态 | 自创新表情 |
| 一屏 ≤2 个 mascot | 满屏 mascot |
| 一屏 ≤2 种渐变 CTA | 5 种渐变全堆 |
| 圆角胶囊或 24-40px | 矩形 / 小圆角扁平按钮 |
| Sticker 必带 4px 4px 0 硬阴影 | Sticker 用普通 box-shadow |

### 11.2 字体

| ✅ Do | ❌ Don't |
|-------|---------|
| 主字 Plus Jakarta Sans | 用 PingFang 做英文标题 |
| Caveat 只在 ≤10 字鼓励语 | Caveat 当正文 / 标题 |
| Hero 用 Extrabold 800 | Body 用 800（看着像广告） |
| Body ≥ 16px | 中文正文 < 14px |

### 11.3 文案

| ✅ Do | ❌ Don't |
|-------|---------|
| 「due 18h 启动！」 | "距离截止时间还有 18 小时" |
| 「我裂开了 再来 5 题」 | "您的正确率有待提高" |
| 「Coffee 时间 ☕」 | "请注意劳逸结合" |

### 11.4 跟 Cert Master 别混

| ✅ UniMate | ❌ 别用 Cert Master 的 |
|-----------|------------------------|
| 牛小匠 | 企鹅 |
| Coral `#FF7A66` | 考证黄 `#FFC52A` |
| 暖白 `#FFFEF7` | 背景灰 `#F5F6F8` |
| Plus Jakarta Sans | PingFang SC 做主字（fallback OK） |
| 8pt grid | 4pt grid |
| `--um-*` | `--cm-*` |

### 11.5 Code review 自检

PR diff 出现以下立即打回：

- 大块 `bg: #FFFFFF` 没改 → ❌ 必须 `--um-canvas`
- 矩形按钮 / 蓝色 CTA → ❌
- 引入 `@mui/material` / `antd` → ❌
- 文案里出现"您 / 宝子 / 智能化" → ❌
- Sticker 没用 `--um-shadow-sticker` → ❌
- Caveat 用在正文 → ❌
- 出现企鹅 / 考证黄 / `--cm-*` → ❌（那是 Cert Master 的）

---

## 12. Asset 目录映射

```
unimate-ai/
├── index.html                ← 视觉设计系统
├── DESIGN.md                 ← 本文件（完整规范）
├── README.md                 ← 仓库使用说明
├── tokens/
│   ├── tokens.json           ← W3C Design Tokens 源数据
│   └── tokens.css            ← --um-* CSS Variables
├── assets/
│   ├── logo/
│   │   ├── horizontal.png    ← 横版（官网 / 邮件 / 小 banner）
│   │   ├── compact.png       ← 竖版（海报 / PPT / App 启动）
│   │   ├── avatar.png        ← 圆头（头像 / 收藏 / favicon）
│   │   ├── fullbody.png      ← 全身（hero / banner 大场景）
│   │   └── app-icon.png      ← App 图标
│   ├── mascot/               ← 9 个标准态（happy 暂用 champion 占位）
│   │   ├── default.png
│   │   ├── studying.png
│   │   ├── thinking.png
│   │   ├── ai-analyzing.png
│   │   ├── charging.png
│   │   ├── tired.png
│   │   ├── deadline.png
│   │   ├── champion.png
│   │   └── spec-sheet.png    ← ChatGPT spec 原图
│   ├── stickers/             ← 贴纸（一等公民）
│   │   └── lets-study.png
│   ├── decorations/
│   │   └── arrow-curly.png
│   └── _inbox/               ← 待分类素材区
└── .github/workflows/
    └── deploy.yml            ← GitHub Pages 自动部署
```

---

## 13. 跟 Cert Master 的隔离规则

UniMate AI 跟 Cert Master 同属 JR Academy，**严格视觉/品牌隔离**：

| 维度 | **UniMate AI (牛小匠)** | Cert Master (考证匠) |
|------|--------------------------|---------------------|
| Mascot | **牛 🐂** | 企鹅 🐧 |
| Primary | **Coral `#FF7A66`** | 考证黄 `#FFC52A` |
| 主 bg | **暖白 `#FFFEF7`** | 背景灰 `#F5F6F8` |
| 主字体 | **Plus Jakarta Sans** | PingFang SC |
| Accent 字体 | **Caveat**（手写鼓励语） | 无 |
| 网格 | **8pt** | 4pt |
| 圆角偏好 | **lg=24, xl=40**（更圆） | lg=16, xl=24 |
| Sticker | **一等公民**（4px 4px 0 硬阴影） | 无 |
| 渐变 | **first-class**（5 个 grad） | 无（只用实色 + glow） |
| 调性 | **学生 meme + 游戏化** | 专业 + 备考严肃 |
| Tagline | **陪你冲 deadline** | 你的 AI 考证搭子 |
| CSS 前缀 | **`--um-*`** | `--cm-*` |
| 目标用户 | **大学生（海外华人）** | 考证人（在职 + 应届） |

### 隔离实施

- CSS 变量前缀彻底分开（`--um-*` vs `--cm-*`），同一项目可共 import 无冲突
- Mascot 不互换：UniMate 不准出现企鹅，Cert Master 不准出现牛
- Logo / Token / Asset 各自独立 repo（unimate-ai / cert-master）
- 字体不抄：UniMate Plus Jakarta Sans + Caveat；Cert Master PingFang SC

---

## 维护

- 每次改 token 必须三处同步：`tokens.json` / `tokens.css` /（如果以后加）`tokens.ts`
- 改了组件规范要在 `index.html` 同步更新视觉示例
- 改了 mascot 或 logo 必须同步更新本文件 §3 / §7 / §12
- 加新 sticker / decoration 要同步更新 §7

### Sources of truth 优先级

```
DESIGN.md  ←  最高（决策源头 / 设计意图）
   ↓ 落地
tokens.json  ←  机器可读的真相（Style Dictionary / Figma Tokens）
   ↓ 翻译
tokens.css  ←  CSS Variables 实现
   ↓ 示例
index.html  ←  视觉手册 / 实景演示
```

- **冲突时**：以 DESIGN.md 为准 — 它代表"为什么这么设计"的人类意图
- **改 DESIGN.md 必须立刻同步**：tokens.json → tokens.css → index.html
- **token 不能擅自改**：手抖把 `#FF7A66` 写成 `#FF7A67` → 按 DESIGN.md 改回来
- **DESIGN.md 才是给设计师/PM 改的**；token 是给前端/设计工具读的

---

_v0.2 · 2026-05-11 · JR Academy_
