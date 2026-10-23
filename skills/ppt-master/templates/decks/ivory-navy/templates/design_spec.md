---
deck_id: ivory-navy
kind: deck
category: brand
summary: 科技、B2B、企业数字化与 AI Agent 报告，用于建立专业可信的论述并推动评审；采用象牙白与深蓝强调风格。
keywords: ["科技", "B2B", "企业数字化", "AI Agent"]
primary_color: "#12355B"
canvas_format: ppt169
canvas_width: 1280
canvas_height: 720
canvas_viewbox: "0 0 1280 720"
replication_mode: standard
native_structure_mode: structured
page_count: 5
---

# 象牙白+深藍強調 — Design Specification

## I. Template Overview

| Application context | Definition |
| --- | --- |
| Recurring presentation family | 科技、B2B、企业数字化与 AI Agent 报告 |
| Intended audiences and outcomes | 面向管理层、评审者、客户与合作方；帮助受众快速理解分析、证据与建议，并推进决策或下一步行动 |
| Delivery and reading assumptions | 以现场讲解为主，同时允许会后独立阅读；页面需保留关键结论、证据标签与必要上下文 |
| Representative narrative/page roles | 当前原型覆盖封面、目录、章节、开放内容和结束语；具体选页、重复、顺序与内容处理由当前项目的 Strategist 根据材料决定 |

- 视觉以#12355B主色、#F7F6F0底色内容页、方形章节编号与简洁网格为识别核心，强调专业、克制与清晰。
- 结构上分为两个可复用 Master 家族：象牙白+深藍強調 Dark 服务封面、章节与收尾，象牙白+深藍強調 Light 服务目录与正文；它们按深浅视觉体系分工，不是按单个 Layout 拆分出的重复 Master。

## II. Color Scheme

| Role | Color | Application |
| --- | --- | --- |
| Primary | #12355B | 深色页面背景、章节编号块、结构线 |
| Accent | #3D6B9E | 强调线、装饰元素 |
| Background | #F7F6F0 | 内容页背景 |
| Panel | #ECEAE0 | 内容承载区 |
| Border | #D9D6C6 | 分隔线和面板边界 |
| Text | #101820 | 内容页标题和正文 |
| White | #FFFFFF | 深色页面文字 |

## III. Typography

| Role | Font stack | Application |
| --- | --- | --- |
| Chinese title and body | `"Microsoft YaHei", "PingFang SC", Arial, sans-serif` | 标题、正文、目录项与联系信息 |
| Latin label and folio | `Arial, "Microsoft YaHei", sans-serif` | 英文机构名、编号、页码与短标签 |

字体栈仅使用常见系统字体；Windows 优先微软雅黑，macOS 可回退苹方，不依赖额外字体安装。

## IV. Signature Design Elements

- 白底内容页使用“主色方形章节号 + 左对齐标题”的稳定页眉，右上角不放置图片 Logo。
- 封面、章节页和结束页保留主色深底、低透明度圆形与细网格线，不引入复杂渐变或动态图片依赖。
- 象牙白+深藍強調 Dark Master 统一承载主色背景和上下结构线；章节页与结束页各自保留圆形几何，封面不继承圆形。象牙白+深藍強調 Light Master 统一承载底色、章节号方块、分隔线和底部主色线。
- 目录页延续数字与双竖线的行式导航。
- 通用内容 carrier 从 slot bounds 左上角开始；封面、章节页、结束页以及小型章节号属于短焦点内容，允许在完整 bounds 内居中。

## V. Page Roster

| File | Master | Layout key | PowerPoint picker name | Visual character | Reusable slots |
| --- | --- | --- | --- | --- | --- |
| `01_cover.svg` | 象牙白+深藍強調 Dark | cover | Cover | 主色背景、居中标题簇与强调线 | 标题、副标题、单位、英文单位 |
| `02_toc.svg` | 象牙白+深藍強調 Light | agenda | Agenda | 数字双竖线目录 | 页面标题、五个目录项、页码 |
| `03_chapter.svg` | 象牙白+深藍強調 Dark | section | Section Header | 主色章节页、居中章节号和标题 | 章节号、章节标题、章节副标题 |
| `04_content.svg` | 象牙白+深藍強調 Light | content | Title and Content | 主色章节号页眉与开放内容面板 | 章节号、页面标题、内容对象、页码 |
| `05_ending.svg` | 象牙白+深藍強調 Dark | closing | Closing | 主色网格背景、居中标题与结束语 | 结束标题、英文副标题、联系信息、页脚 |
