# 🖥️ HarnessDesk — DeepSeek Harness, Right on Your Desktop

[English](README.en.md) | 简体中文

> 🌐 Website: [harnessdesk.hibcglobal.com](https://harnessdesk.hibcglobal.com)
> 📦 Download: [Windows Installer](https://github.com/HBC-Tech-coder/HarnessDesk/releases/download/legacy-preview-0.1.0-rc.6/DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe)
> ⭐ GitHub: [HBC-Tech-coder/HarnessDesk](https://github.com/HBC-Tech-coder/HarnessDesk)

---

## 🔥 100K Stars in 48 Hours — Now Everyone Can Use It

On August 13, DeepSeek open-sourced **DeepSeek Harness**, an Agent framework built on the philosophy that "everything is a plugin." In less than 48 hours, it crossed **100,000 GitHub Stars**.

The verdict from early testers is unanimous: **it works — but it's not for everyone.**

- Requires Node.js
- Requires command-line setup (`npx @deepseek-ai/dsh web`)
- Requires plugin configuration, API keys, and workspace setup

For non-developers, that barrier is enough to turn away 90% of people who want to try it.

**HarnessDesk exists to fix that.**

We package DeepSeek Harness into a self-contained Windows desktop app — **double-click to install, no environment setup, no command line, just open and go.**

---

## ✨ What Can HarnessDesk Do?

| Feature | Status |
|---|---|
| 🖥️ Windows desktop client (Electron, self-contained runtime) | ✅ Available |
| 🔑 Bring-your-own DeepSeek API Key (BYOK) | ✅ Available |
| 👤 Unified account + free credits on signup | 🟡 In development |
| 🎭 Live2D animated desktop companion | 🟡 In development |
| 🔄 Auto-update | 🟡 In development |
| 🍎 macOS client | ⏳ Planned |

---

## 🚀 Get Started in 3 Steps

### 1️⃣ Download & Install

[⬇️ Download Windows Installer](https://github.com/HBC-Tech-coder/HarnessDesk/releases/download/legacy-preview-0.1.0-rc.6/DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe) (175 MB)

> ⚠️ The installer is not yet code-signed. Windows SmartScreen may show a warning. Click "More info" → "Run anyway" to proceed.

### 2️⃣ Enter Your API Key

Launch HarnessDesk and enter your DeepSeek API Key in Settings.

Don't have a key? No problem — our **unified account + free credits** feature is coming soon. Sign up and get free credits without applying for your own key.

### 3️⃣ Start Working

Pick a local workspace and let Harness write code, handle files, and invoke plugins for you.

---

## 🛡️ We Don't Fork the Core

HarnessDesk is a compatibility layer. All product-level additions — desktop runtime, account system, pluggable character layer — sit on top of the upstream open-source DeepSeek Harness without modifying its core.

This means: **every upstream update reaches you quickly. You're always running the latest Harness.**

Upstream: [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) (MIT License)

---

## 🔒 Security & Privacy

- No platform API key is bundled in the installer
- Your API key is stored locally and never uploaded to our servers
- Community credits (in development) are proxied through a controlled server; the master key is never sent to your device
- For security issues, do NOT post keys in public Issues. Use [GitHub Private Vulnerability Reporting](https://github.com/HBC-Tech-coder/HarnessDesk/security/advisories/new)

---

## 🗺️ Roadmap

- [x] Windows desktop client + self-contained runtime
- [ ] Unified account + free credits + top-up
- [ ] Live2D animated companion
- [ ] Auto-update
- [ ] macOS client
- [ ] Integrate more AI tools

---

## ⚠️ Unofficial Disclaimer

HarnessDesk is an independently maintained **unofficial community client**. It is not affiliated with, authorized by, sponsored by, or endorsed by DeepSeek AI. The terms "DeepSeek" and "DeepSeek Harness" are used solely to identify the compatible upstream open-source project.

---

## 📄 License

MIT License
