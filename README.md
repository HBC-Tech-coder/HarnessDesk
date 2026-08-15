# HarnessDesk

[English](README.en.md) | 简体中文

> **当前发布是有第一版 HarnessDesk 正式版。**
>
> 安装包未签名，可能触发 Windows SmartScreen；本机独立复验中安装成功。

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
