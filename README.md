# HarnessDesk

# 🖥️ HarnessDesk — 把 DeepSeek Harness 装进你的电脑

[English](README.en.md) | 简体中文

> 🌐 官网：[harnessdesk.hibcglobal.com](https://harnessdesk.hibcglobal.com)
> 📦 一键下载：[Windows 安装包](https://github.com/HBC-Tech-coder/HarnessDesk/releases/download/legacy-preview-0.1.0-rc.6/DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe)
> ⭐ GitHub：[HBC-Tech-coder/HarnessDesk](https://github.com/HBC-Tech-coder/HarnessDesk)

## 🔥 两天 10 万 Star 的 DeepSeek Harness，普通人终于能用了

8 月 13 日晚，DeepSeek 开源了 Agent 运行框架 **DeepSeek Harness**，核心理念"一切皆插件"，上线不到 48 小时 GitHub Star 突破 **10 万**。

媒体实测结论很一致：**能干活，但得盯着；普通用户有门槛。**

- 要装 Node.js 环境
- 要敲命令行 `npx @deepseek-ai/dsh web`
- 要配插件、配 API Key、配工作区

对于不会写代码的普通用户，这道门槛劝退了 90% 的人。

**HarnessDesk 就是来解决这个问题的。**

我们把 DeepSeek Harness 打包成一个自包含的 Windows 桌面软件——**双击安装，不用配环境，不用敲命令，打开就能用。**

## ✨ HarnessDesk 能做什么？

| 能力 | 状态 |
|---|---|
| 🖥️ Windows 桌面端（Electron，自包含运行环境） | ✅ 已上线 |
| 🔑 自带 DeepSeek API Key（BYOK 模式） | ✅ 已上线 |
| 👤 统一账号 + 注册赠送额度 | 🟡 开发中 |
| 🎭 Live2D 动态桌面伴侣 | 🟡 开发中 |
| 🔄 自动更新 | 🟡 开发中 |
| 🍎 macOS 客户端 | ⏳ 规划中 |

---

## 🚀 三步开始使用

### 1️⃣ 下载安装

[⬇️ 点击下载 Windows 安装包](https://github.com/HBC-Tech-coder/HarnessDesk/releases/download/legacy-preview-0.1.0-rc.6/DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe)（175 MB）

> ⚠️ 安装包尚未代码签名，Windows SmartScreen 可能提示。点击"更多信息"→"仍要运行"即可。

### 2️⃣ 填入 API Key

启动 HarnessDesk，在设置中填入你的 DeepSeek API Key。

没有 Key？没关系——我们正在开发**统一账号 + 注册赠送额度**功能，上线后注册即送，不用自己申请。

### 3️⃣ 开始干活

选择本地工作区，让 Harness 帮你写代码、处理文件、调用插件。

---

## 🛡️ 我们不改 Harness 核心

HarnessDesk 作为兼容层，把产品增量放在**桌面运行环境、账户入口和可插拔人物层**，核心逻辑 100% 遵循上游开源 DeepSeek Harness。

这意味着：**官方每次更新，我们都能快速跟进，你永远用的是最新版 Harness。**

上游项目：[deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)（MIT 协议）

---

## 🔒 安全与隐私

- 安装包不内置平台主 API Key
- 用户 API Key 存储在本地，不上传服务器
- 社区额度（开发中）通过服务端受控中转，主 Key 不下发设备
- 安全问题请勿在公开 Issue 中提交密钥，请使用 [GitHub Private Vulnerability Reporting](https://github.com/HBC-Tech-coder/HarnessDesk/security/advisories/new)

---

## 🗺️ 路线图

- [x] Windows 桌面端 + 自包含运行环境
- [ ] 统一账号 + 注册赠送额度 + 充值
- [ ] Live2D 动态伴侣
- [ ] 自动更新
- [ ] macOS 客户端
- [ ] 整合更多 AI 工具（三生、Aistory 等）

---

## ⚠️ 非官方声明

HarnessDesk 是独立维护的**非官方社区客户端**，与 DeepSeek AI 无隶属、授权、赞助或官方背书关系。"DeepSeek"与"DeepSeek Harness"仅用于说明兼容的上游开源项目。


## 📄 许可证

MIT License

HarnessDesk 是独立维护的非官方社区客户端，与 DeepSeek AI 无隶属、授权、赞助或官方背书关系。“DeepSeek”与“DeepSeek Harness”仅用于说明兼容的上游开源项目，以及识别旧安装包中无法改写的历史元数据。

## 下载

请从 [GitHub Releases](https://github.com/HBC-Tech-coder/HarnessDesk/releases) 下载，并只接受以下精确资产：


下载后请先阅读 [校验与 SmartScreen 说明](docs/VERIFY_DOWNLOADS.md)。

## 包含与不包含

安装包归档结构包含 Electron 客户端、Node.js 运行时、Harness 运行闭包及依赖。安装程序允许选择安装目录，并创建桌面、开始菜单和卸载入口。

以下能力属于即将开发的内容：统一账号、短信、赠送额度、平台代理、Hosted BYOK、充值、动态 Live2D/Cubism。

## 上游与许可

交接记录指向上游 deepseek-ai/deepseek-harness commit [47f943859bef60e4160492346772ded9b24f765a](https://github.com/deepseek-ai/deepseek-harness/commit/47f943859bef60e4160492346772ded9b24f765a)，根包版本为 0.1.0-rc.5，处于 developer preview。该提交不是 HarnessDesk 当前候选，也不表示本仓库发布了上游源码。

仓库保留 MIT 许可、上游原始 MIT 文本和上游第三方声明。安装包没有在应用根目录携带上游根 LICENSE / THIRD_PARTY_NOTICES，这是已知的旧包装限制；本 Release 将这些文档作为伴随资产公开，但不把该补充描述成新包已通过完整法律门禁。

## 安全报告

请勿在公开 Issue 中提交密钥、Cookie、验证码、私聊、日志全文或其他隐私数据。安全问题请使用 [GitHub Private Vulnerability Reporting](https://github.com/HBC-Tech-coder/HarnessDesk/security/advisories/new)。
