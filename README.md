<div align="center">

# 📚 zzhscheduler — 自动排课系统

**Auto Course Scheduler · 云端账号系统 · Serverless · 开箱即用**

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-4f6ef7?style=for-the-badge&logo=github)](https://ablu6669.github.io/zzhscheduler/)
[![Version](https://img.shields.io/badge/Version-3.2.0-f59e0b?style=for-the-badge)]()
[![CloudBase](https://img.shields.io/badge/Backend-Tencent%20CloudBase-4f6ef7?style=for-the-badge&logo=tencentqq)]()

[🚀 立即体验 / Live Demo](https://ablu6669.github.io/zzhscheduler/) · [📮 反馈 / Feedback](#反馈--feedback)

---

</div>

## 🌟 这是什么？/ What is this?

**自动排课系统**帮助大学生在选课时，从数十种可能的组合中快速筛选出最优课表方案。

**Auto Course Scheduler** helps university students quickly find the optimal timetable from all possible course combinations.

> 5 门课各 3 个时段 → 243 种组合。这个工具几秒内帮你找到最优方案。
> 5 courses × 3 slots each = 243 combinations. This tool finds the best one in seconds.

输入每门课的可用时段 → 设置筛选条件 → 一键生成所有可行方案，按你的偏好排序。前端纯 HTML 单文件 + 腾讯云开发后端，轻量但完整。

Enter available time slots → set filters → generate all feasible schedules, sorted by your preferences. Single HTML file frontend + Tencent CloudBase backend — lightweight yet complete.

---

## ✨ 核心功能 / Features

| 功能 / Feature | 说明 / Description |
|------|------|
| 🗓️ **智能枚举 / Smart Enumeration** | 自动枚举所有课程时段的可行组合，无遗漏 / Automatically enumerate all feasible combinations, no omissions |
| 🚫 **智能筛选 / Smart Filtering** | 一键排除早八、午一；自定义排除时间段和地点 / One-click exclude early morning / noon classes; custom time & location exclusions |
| ⚖️ **多维排序 / Multi-dimensional Sorting** | 按时间（支持自定义时段权重）、地点相邻距离（支持自定义地点权重）、自定义权重多维度排序 / Sort by time (custom time weights), location adjacency (custom location weights), or custom weights |
| 🔗 **子课程支持 / Sub-course Support** | 主课 + 子课（Lec + Tut）联排，排课更合理 / Link Lecture & Tutorial sessions for more reasonable scheduling |
| 📊 **Excel 一键导出 / One-click Excel Export** | 导出完整课表 Excel，含课程列表和时间表 / Export full schedule with course list and timetable |
| 🌐 **中英双语 / Bilingual UI** | 界面支持中文 / English 切换 / Switch between Chinese and English interface |
| 🔐 **云端账号 / Cloud Account** | 基于 Tencent CloudBase，账号系统 + 使用额度管理 / Account system with usage quota management via CloudBase |
| 📢 **公告推送 / Announcements** | 管理员发布公告，用户端实时查看 / Admin-published announcements with real-time user notifications |
| 💾 **本地缓存 / Local Cache** | 课程数据存 localStorage，刷新不丢失 / Course data saved in localStorage, survives refresh |
| ✏️ **时段直接编辑 / Edit Sessions** | 直接编辑已有时段，无需删除重建 / Edit existing sessions directly, no need to delete and re-add |
| ☑️ **参与排课开关 / Schedule Toggle** | 灵活勾选哪些时段参与计算 / Control which sessions are included in schedule calculation |
| 🔒 **时间校验 / Time Validation** | 结束时间不得早于开始时间 / End time cannot be earlier than start time |
| ⚡ **剪枝优化 / Pruning Optimization** | 增量剪枝 + 位运算加速 + 智能枚举顺序 + 分支限界 + 安全截断，枚举全部可行方案后排序选最优 / Incremental pruning + bitmask + smart ordering + branch-and-bound + safe truncation (min 5000 plans) |
| ⚠️ **组合数预警 / Combo Warning** | 超大数据量时自动提醒用户 / Auto-warn when combinations are too large |

---

## 🚀 快速开始 / Quick Start

**方式一：直接在线体验（推荐）/ Option 1: Try Online (Recommended)**

→ 打开 / Open [https://ablu6669.github.io/zzhscheduler/](https://ablu6669.github.io/zzhscheduler/)

> 🎉 **GitHub 体验账号 / Trial Account**：`githubers` / `githubers`（无限额度，欢迎随便玩！/ Unlimited quota, feel free to explore!）
>
> 登录后即可体验完整功能，无需注册。体验后欢迎提 Issue 或邮件反馈！
> Login to experience all features — no registration needed. Feedback via Issue or email welcome!

**方式二：本地部署 / Option 2: Local Deploy**

```bash
git clone https://github.com/asuskurumi/zzhscheduler.git
cd zzhscheduler
# 直接用浏览器打开 index.html 即可体验前端功能
# Open index.html in your browser to try the frontend
open index.html
```

整个项目只有一个 `index.html` 文件。/ The entire project is a single `index.html` file.

---

## 📖 使用流程 / How to Use

```
1. 添加课程   → 输入课程代号（如 MAT1001），添加各时段信息
2. 配置筛选   → 选择不上早八、不上午一，或自定义排除条件
3. 选择排序   → 按时间紧凑 / 地点临近 / 自定义权重排序
4. 计算方案   → 点击「计算排课方案」，查看所有可行排课
5. 导出课表   → 选择喜欢的方案，一键导出 Excel
```

```
1. Add Courses    → Enter course codes (e.g. MAT1001), add session details
2. Set Filters    → Exclude early morning / noon, or set custom exclusions
3. Choose Sorting → Sort by time compactness / location proximity / custom weights
4. Calculate      → Click "Calculate Schedule" to see all feasible options
5. Export         → Pick your favorite plan, one-click export to Excel
```

---

## 🖼️ 界面预览 / Screenshots

> 登录界面 → 课程管理 → 筛选排序 → 排课结果 → 导出 Excel
> Login → Course Management → Filters & Sorting → Results → Excel Export

（欢迎 star 后截图分享你的课表 👇 / Share your schedule screenshot after starring! 👇）

---

## 🔧 技术栈 / Tech Stack

| 技术 / Tech | 说明 / Description |
|------|------|
| **前端 / Frontend** | HTML + CSS + Vanilla JavaScript，零框架依赖 / Zero framework dependency |
| **后端 / Backend** | [腾讯云开发 CloudBase](https://tcb.cloud.tencent.com/)（账号系统、使用额度、公告管理）/ Account, quota & announcement management |
| **数据持久化 / Persistence** | 课程数据存 `localStorage`，账号与公告走云端 / Course data in localStorage, accounts & announcements in cloud |
| **Excel 导出 / Excel Export** | [xlsx-js-style](https://github.com/gitbrent/xlsx-js-style)（支持单元格样式）/ With cell styling support |
| **部署 / Deployment** | GitHub Pages（前端）+ 腾讯云 SCF（后端接口），推送即上线 / Push to deploy |

---

## 🗺️ Roadmap

### ✅ 已完成 / Done

- [x] 子课程链接（Lec & Tut 联排）/ Sub-course linking (Lec & Tut)
- [x] 滚轮 + 手动输入时间选择 / Scroll wheel + manual input time picker
- [x] 使用说明模块 / User guide module
- [x] 时间 / 地点优先权重个性化 / Custom time & location priority weights
- [x] ABE 地点支持 / ABE location support
- [x] 用户分级与使用额度限制 / User tier & usage quota system
- [x] 消息通知窗口（公告栏）/ Announcement panel
- [x] 自定义权重排序（如教授偏好）/ Custom weight sorting (e.g. professor preference)
- [x] 一键导出 Excel 课表 / One-click Excel schedule export
- [x] 中英双语切换 / Bilingual UI (Chinese / English)
- [x] 参与排课开关（定向选择）/ Schedule toggle per session
- [x] 已有时段直接编辑 / Direct session editing
- [x] 时间选择灵敏度优化 + 箭头步进 / Reduced scroll sensitivity + arrow step buttons
- [x] 地点排序逻辑优化（只算 2 小时内间隔）/ Location sorting: only sessions within 2h
- [x] 腾讯云开发（CloudBase）后端 / Tencent CloudBase backend
- [x] 云端额度同步（跨浏览器）/ Cloud quota sync across browsers
- [x] 管理员后端直连管理（账号 / 通知）/ Admin direct DB management
- [x] 管理员公告一键翻译 / Admin one-click announcement translation
- [x] 时段时间校验（结束 ≥ 开始）/ Time validation (end ≥ start)
- [x] 多筛选项优先级排序 / Multi-filter priority sorting
- [x] 剪枝优化（增量剪枝 + 位运算 + 智能枚举 + 分支限界 + 安全截断）/ Pruning optimization (incremental pruning + bitmask + smart ordering + branch-and-bound + safe truncation)
- [x] 组合数预警提示 / Combination count warning
- [x] 降本增效优化（合并额度 API 为单次调用 + 公告/版本号 24h 前端缓存）/ Cost reduction (merge quota API to single call + 24h frontend cache for announcements/version)

### 🔲 计划中 / Planned

- [ ] 微信小程序版本 / WeChat Mini Program version
- [ ] 学分计算 / Credit calculation
- [ ] 课程数据源对接 / Course data source integration

---

## 反馈 / Feedback

使用中遇到 bug、有功能建议？欢迎：/ Found a bug or have a suggestion? Reach out:

- 📮 发邮件 / Email：[abluzz@outlook.com](mailto:abluzz@outlook.com)
- 🐛 提 Issue / Open Issue：[GitHub Issues](https://github.com/asuskurumi/zzhscheduler/issues)

内测期间，所有被采纳的反馈将获赠高额度公测账号奖励！/ All adopted feedback earns a premium account reward during beta!

---

<div align="center">

如果这个项目对你有帮助，欢迎点个 ⭐ Star！
If this project helps you, please consider giving it a ⭐ Star!

</div>
