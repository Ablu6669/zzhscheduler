# 智链简历 (SmartChain Resume)

<div align="center">

**AI 驱动的智能简历系统与云端招聘解决方案**

[在线演示](https://Ablu6669.github.io/zzh_resume-system) · [问题反馈](https://github.com/Ablu6669/zzh_resume-system/issues)

</div>

---

## 📖 项目简介

**智链简历**是一款面向线下招聘会场景的智能简历系统，致力于解决招聘会现场简历格式混乱、数据难以结构化的痛点。

求职者通过标准化模板填写简历并生成唯一识别码；企业端扫码或输入识别码即可快速查询、预览、导出简历，实现招聘数据的高效流转。

> 💡 本项目为 **腾讯学堂 AI-HR 线上实战营** 自定义赛道作业 Demo。

---

## ✨ 功能特性

### 👤 求职者端
- 📝 **标准化简历编辑** — 多步骤表单引导，结构化管理个人信息、教育经历、工作经历、项目经历、技能特长
- 🎨 **实时预览** — 编辑同时实时渲染简历效果，所见即所得
- 📄 **PDF 导出** — 一键生成高质量 PDF 简历文件
- ☁️ **云端保存** — 简历数据加密存储至 GitHub Gist，生成唯一识别码便于分享

### 🏢 企业端
- 🔍 **识别码查询** — 输入求职者分享的识别码，秒级调出简历
- 👁️ **在线预览** — 直接在浏览器中查看完整简历内容
- 📊 **Excel 批量导出** — 支持将简历数据导出为 Excel 格式，便于企业 HR 统一管理
- 📱 **移动端适配** — 响应式设计，支持手机 / 平板 / 电脑多端访问

---

## 🏗️ 系统架构

```
┌─────────────────┐     HTTPS      ┌──────────────────────┐     GitHub API     ┌─────────────────┐
│   浏览器前端     │ ────────────>  │  腾讯云 SCF 云函数   │ ────────────>  │  GitHub Gist    │
│  (Single File) │ <────────────   │  (服务端代理)        │ <────────────   │  (云端存储)      │
└─────────────────┘     JSON       └──────────────────────┘     JSON          └─────────────────┘
        │                                                      │
        │                                                      │
        v                                                      v
┌─────────────────┐                                  ┌─────────────────┐
│  localStorage   │                                  │  GitHub Token   │
│  (本地缓存)     │                                  │  (仅服务端持有)  │
└─────────────────┘                                  └─────────────────┘
```

### 架构亮点

| 设计点 | 说明 |
|--------|------|
| **Token 安全** | GitHub Token 仅存在于 SCF 服务端，前端代码零敏感信息 |
| **国内访问** | 腾讯云 SCF 国内节点，避免 Cloudflare Workers 国内无法访问问题 |
| **零成本运行** | SCF 按调用计费 + GitHub Gist 免费存储，个人使用近乎免费 |
| **单文件部署** | Vite 打包为单个 HTML 文件，通过 GitHub Pages 免费托管 |

---

## 🛠️ 技术栈

### 前端
- **框架**：React 19 + TypeScript
- **构建工具**：Vite 8 + vite-plugin-singlefile
- **样式**：Tailwind CSS 3 + Lucide React 图标库
- **路由**：React Router DOM 7
- **导出**：jsPDF (PDF) + SheetJS xlsx (Excel)
- **二维码**：qrcode.react

### 后端
- **云服务**：腾讯云 SCF (Serverless Cloud Function)
- **存储**：GitHub Gist API
- **安全代理**：SCF 函数作为前端与 GitHub API 之间的代理层，Token 仅存在于服务端

### 部署
- **静态托管**：GitHub Pages
- **单文件输出**：`dist-single/index.html`

---

## 📌 已知问题与改进方向

- [ ] 增加用户账号体系，支持多份简历管理
- [ ] 企业端支持批量导入识别码、批量导出 PDF
- [ ] 简历模板多样化，支持更多排版风格
- [ ] 接入 AI 能力，实现简历内容智能优化建议

---

## 📄 License

本项目采用 [Apache License 2.0](./LICENSE) 开源。

允许商用、修改和分发，但须保留原作者版权声明。详见 [LICENSE](./LICENSE) 文件。

---

## 🙏 致谢

- 腾讯学堂 AI-HR 线上实战营提供的项目方向指导
- [React](https://react.dev/)、[Vite](https://vitejs.dev/)、[Tailwind CSS](https://tailwindcss.com/) 等开源项目
- [GitHub Gist](https://gist.github.com/) 提供的免费存储服务
- [腾讯云 SCF](https://cloud.tencent.com/product/scf) 提供的 Serverless 计算能力

---

<div align="center">

**⭐ 如果这个项目对你有帮助，欢迎 Star！**

</div>
