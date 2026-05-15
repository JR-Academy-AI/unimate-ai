# UniMate AI · App Design References

> 仅供团队对齐用 · 不照搬开发 · 实现以产品 PRD 为准

这 4 张是设计师产出的 App 视觉稿。看法跟 `cert-master/assets/app-design-refs/` 一样 —— **学 mascot 用法 / 配色调性 / 信息架构**，不复制像素。

视觉手册：[`../../app-design-refs.html`](../../app-design-refs.html)（双击打开）。
完整品牌规范：[`../../DESIGN.md`](../../DESIGN.md) + [`../../index.html`](../../index.html)。

| # | 文件 | 内容 | 关键点 |
|---|------|------|--------|
| 01 | `01-home.png` | App 首页 | "今天想<u>学</u>什么？" hero + 5 入口 + 热门课程 4 卡 + Lv.12 进度 + 大家都在问 |
| 02 | `02-auth.png` | 登录 / 注册（2-up） | UNSW 学号优先登录 / 4 选 1 + 注册表单 + 三方登录 |
| 03 | `03-course-intel-community.png` | 选课情报局 8 张关联页 | 水课榜 / Tutor 评分 / 投票广场 / 帖子流 / 个人中心 — UniMate 杀手级社区 ① |
| 04 | `04-core-features.png` | 9 个核心功能 + 8 mascot 表情库 | 启动 / 首页 / 课表 / AI 助手 / 复习卡 / DDL / Widget / 进度 / 我的 |
| 05 | `05-academic-risk-rescue.png` | 学术风险救援站 3 大功能 + 6 张页 | 理解作业 + Turnitin 23% 风险检测 + 学术警告应对 — UniMate 杀手级救援 ② |
| 06 | `06-ai-timetable-import.png` | AI 导入课表 6 步流程 | 学校 OAuth / 文件上传 / 文本粘贴 / 手动 4 选 1 → AI 识别 98% → 周视图 |
| 07 | `07-niu-quan-campus-feed.png` + `07b-niu-quan-ipad.png` | 牛圈 · 校园 Feed (mobile + iPad) | 顶部 5 tab（推荐/活动/课程/社区/搭子）+ AI 校园助手 hero + 活动 banner + 牛课榜 + 新生任务 + UGC + 学习搭子 — UniMate 校园社交聚合 ③ |

---

## Mascot 用法速查（按场景）

| 场景 | Mascot 状态 |
|------|-------------|
| 首页 Hero | `studying`（笔记本前学习） |
| 等级进度 / 升级 | `champion`（戴学位帽 / 满分） |
| DDL 倒计时 | `anxious` / `sprint`（火焰款 — 紧迫感） |
| AI 助手聊天 | `ai-analyzing`（扫描眼） |
| 复习卡片 | `studying`（拿书） |
| 登录注册 hero | `happy`（挥手 / waving） |
| 我的 / Profile 主页 | `happy`（不要焦虑感） |

完整 mascot 决策树 → `../../DESIGN.md` §3。

---

## 红线（CERT MASTER / JOB HUNTER 隔离）

- ❌ 不要把这里的图复用到 cert-master / job-hunter 的 brand 文档 — 三方品牌严格视觉隔离
- ❌ Mascot 服装不要换西装 + 公文包（那是 Job Hunter 求职牛）
- ❌ 不要在 UniMate 资产里出现企鹅（那是 Cert Master）
- ❌ 主色 `--um-coral` `#FF7A66` 不要换成 `--cm-yellow` `#FFC52A` 或 `--jh-primary` `#5F7CFB`

源 spec 图：上传日 **2026-05-14** · 设计师 ChatGPT collab。
