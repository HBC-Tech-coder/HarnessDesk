# HarnessDesk

[English](README.en.md) | 简体中文

> **当前发布是有已知故障的旧版预览（Legacy Preview），不是 HarnessDesk 当前正式版。**
>
> 旧安装包未签名，可能触发 Windows SmartScreen；本机独立复验中安装成功，但连续两次冷启动都因缺少打包模块而失败。请勿用于生产环境或日常工作。

HarnessDesk 是独立维护的非官方社区客户端，与 DeepSeek AI 无隶属、授权、赞助或官方背书关系。“DeepSeek”与“DeepSeek Harness”仅用于说明兼容的上游开源项目，以及识别旧安装包中无法改写的历史元数据。

## 下载

请从 [GitHub Releases](https://github.com/HBC-Tech-coder/HarnessDesk/releases) 下载，并只接受以下精确资产：

| 字段 | 值 |
|---|---|
| 发布轨道 | Legacy Preview / 旧版预览 |
| 文件名 | DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe |
| 大小 | 183,666,660 bytes（175.16 MiB） |
| SHA-256 | B16ABD84241A1515C15698BE1B21C391AE520E3FFDC4BFCB7FBC93C9A4F92407 |
| Authenticode | NotSigned |
| 更新状态 | 内置更新 URL 为空，默认关闭 |
| 源码 | 本仓库不发布此安装包的产品源码 |

下载后请先阅读 [校验与 SmartScreen 说明](docs/VERIFY_DOWNLOADS.md)。

## 本机复验结果

复验环境：Windows 11 专业版 64 位，build 26200，x64；时间 2026-08-15 +08:00。

| 项目 | 状态 | 证据摘要 |
|---|---|---|
| 精确文件、大小、SHA-256 | PASS | 与上表完全一致 |
| Authenticode | NotSigned | 无代码签名证书 |
| Microsoft Defender | PASS | 安装包与完整解包目录均为 0 threats |
| Gitleaks 8.30.1 | PASS | 完整解包目录及 app.asar 均为 0 findings |
| 模型 / Live2D / Cubism 路径 | PASS | 33,376 个解包文件中命中 0 |
| 安装 | PASS | 安装器退出码 0；安装目录、桌面/开始菜单快捷方式和卸载入口均创建 |
| 第一次冷启动 | FAIL | 未建立 loopback 服务；缺少 ./machine-id/getMachineId |
| 第二次冷启动 | FAIL | 同一错误再次出现 |
| 卸载 | PARTIAL / FAIL | 卸载器退出码 0，进程/注册表/快捷方式清零；60 秒后仍残留 17 个长路径文件 |
| 自动更新 | DISABLED | resources/update-config.json 的 URL 为空；未连接 HarnessDesk 新更新链路 |

完整事实矩阵见 [旧版预览发布说明](docs/LEGACY_PREVIEW_0.1.0-rc.6.md) 和 [审计 manifest](legacy-preview-0.1.0-rc.6.manifest.json)。

## 包含与不包含

安装包归档结构包含 Electron 客户端、Node.js 运行时、Harness 运行闭包及依赖。安装程序允许选择安装目录，并创建桌面、开始菜单和卸载入口。

以下能力不属于这个旧版预览的已验证能力：统一账号、短信、赠送额度、平台代理、Hosted BYOK、充值、动态 Live2D/Cubism、生产更新 feed，以及可复现的源码到二进制构建。因为冷启动失败，界面与核心 Harness 工作流也不得视为已验证。

## 上游与许可

旧包交接记录指向上游 deepseek-ai/deepseek-harness commit [47f943859bef60e4160492346772ded9b24f765a](https://github.com/deepseek-ai/deepseek-harness/commit/47f943859bef60e4160492346772ded9b24f765a)，根包版本为 0.1.0-rc.5，处于 developer preview。该提交不是 HarnessDesk 当前候选，也不表示本仓库发布了上游源码。

仓库保留 MIT 许可、上游原始 MIT 文本和上游第三方声明。旧安装包没有在应用根目录携带上游根 LICENSE / THIRD_PARTY_NOTICES，这是已知的旧包装限制；本 Release 将这些文档作为伴随资产公开，但不把该补充描述成新包已通过完整法律门禁。

## 安全报告

请勿在公开 Issue 中提交密钥、Cookie、验证码、私聊、日志全文或其他隐私数据。安全问题请使用 [GitHub Private Vulnerability Reporting](https://github.com/HBC-Tech-coder/HarnessDesk/security/advisories/new)。
