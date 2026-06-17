<div align="center">

# 📚 zzhscheduler — 自动排课系统

**Auto Course Scheduler · 云端账号系统 · 纯网页 · 开箱即用**

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-4f6ef7?style=for-the-badge&logo=github)](https://asuskurumi.github.io/zzhscheduler/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/Version-2.2.0-f59e0b?style=for-the-badge)]()
[![CloudBase](https://img.shields.io/badge/Backend-Tencent%20CloudBase-4f6ef7?style=for-the-badge&logo=tencentqq)]()

[🚀 立即体验 / Live Demo](https://asuskurumi.github.io/zzhscheduler/) · [📮 反馈建议](#反馈--feedback)

---

</div>

## 🌟 这是什么 / What is this?

**自动排课系统**帮助大学生在选课时，从数十种可能的组合中快速筛选出最优课表方案。

> You have 5 courses, each with 3 available time slots — that's 243 possible combinations. This tool finds the best one for you in seconds.

输入每门课的可用时段 → 设置筛选条件 → 一键生成所有可行方案，按你的偏好排序。前端纯 HTML 单文件 + 腾讯云开发后端，轻量但完整。

---

## ✨ 核心功能 / Features

| 功能 | 说明 |
|------|------|
| 🗓️ **智能枚举** | 自动枚举所有课程时段的可行组合，无遗漏 |
| 🚫 **智能筛选** | 一键排除早八、排除午一；支持自定义排除时间段和地点 |
| ⚖️ **多维排序** | 按时间紧凑度、上课地点远近、自定义权重多维度排序 |
| 🔗 **子课程支持** | 支持主课 + 子课（Lecture + Tutorial）联排，排课更合理 |
| 📊 **Excel 一键导出** | 导出完整课表 Excel，含课程列表和时间表 |
| 🌐 **中英双语** | 界面支持中文 / English 切换 |
| 🔐 **云端账号** | 基于腾讯云开发（CloudBase），支持账号系统与使用额度管理 |
| 📢 **公告推送** | 管理员可发布系统公告，用户端实时查看更新通知 |
| 💾 **本地缓存** | 课程数据存于 localStorage，无需担心刷新丢失 |
| ✏️ **时段直接编辑** | 可直接编辑已有时段，无需删除重建 |
| ☑️ **参与排课开关** | 灵活勾选哪些时段参与计算，方便对比方案 |

---

## 🚀 快速开始 / Quick Start

**方式一：直接在线使用（推荐）**

→ 打开 [https://asuskurumi.github.io/zzhscheduler/](https://asuskurumi.github.io/zzhscheduler/)，无需安装，即开即用。

**方式二：本地部署**

```bash
git clone https://github.com/asuskurumi/zzhscheduler.git
cd zzhscheduler
# 直接用浏览器打开 Index.html 即可体验前端功能
open Index.html
```

整个项目只有一个 `index.html` 文件。

---

## 📖 使用流程 / How to Use

```
1. 添加课程  →  输入课程代号（如 MAT1001），添加各时段信息
2. 配置筛选  →  选择不上早八、不上午一，或自定义排除条件
3. 选择排序  →  按时间紧凑 / 地点临近 / 自定义权重排序
4. 计算方案  →  点击「计算排课方案」，查看所有可行排课
5. 导出课表  →  选择喜欢的方案，一键导出 Excel
```

---

## 🖼️ 界面预览 / Screenshots

> 登录界面 → 课程管理 → 筛选排序 → 排课结果 → 导出 Excel

（欢迎 star 后截图分享你的课表 👇）

---

## 🔧 技术栈 / Tech Stack

- **前端** — HTML + CSS + Vanilla JavaScript，零框架依赖
- **后端** — [腾讯云开发 CloudBase](https://tcb.cloud.tencent.com/)（账号系统、使用额度、公告管理）
- **数据持久化** — 课程数据存 `localStorage`，账号与公告走云端
- **Excel 导出** — [xlsx-js-style](https://github.com/gitbrent/xlsx-js-style)（支持单元格样式）
- **部署** — GitHub Pages（前端）+ 腾讯云 SCF（后端接口），推送即上线

---

## 🗺️ Roadmap

- [x] 多维排序 + 权重自定义
- [x] Excel 一键导出
- [x] 中英双语支持
- [x] 子课程 (Tutorial/Lab) 联排
- [x] 时段直接编辑
- [ ] 移动端布局优化
- [ ] 课表截图导出（PNG）
- [ ] 更多高校地图支持

---

## 反馈 / Feedback

使用中遇到 bug、有功能建议？欢迎：

- 📮 发邮件：[15562886669@163.com](mailto:15562886669@163.com)
- 🐛 提 Issue：[GitHub Issues](https://github.com/asuskurumi/zzhscheduler/issues)

内测期间，所有被采纳的反馈将获赠高额度公测账号奖励！

---

## 📄 License

MIT License © 2026 asuskurumi

---

<div align="center">

如果这个项目对你有帮助，欢迎点个 ⭐ Star！  
If this project helps you, please consider giving it a ⭐ Star!

</div>
