# HarnessDesk

English | [简体中文](README.md)

> **The current release is a known-broken Legacy Preview, not the current HarnessDesk production release.**
>
> The legacy installer is unsigned and may trigger Windows SmartScreen. Independent testing installed it successfully, but two consecutive cold starts failed because a packaged module is missing. Do not use it for production or daily work.

HarnessDesk is an independently maintained, unofficial community client. It is not affiliated with, authorized by, sponsored by, or endorsed by DeepSeek AI. “DeepSeek” and “DeepSeek Harness” are used only to identify the compatible upstream open-source project and unavoidable historical metadata inside the legacy installer.

## Download

Download only from [GitHub Releases](https://github.com/HBC-Tech-coder/HarnessDesk/releases), and accept only this exact asset:

| Field | Value |
|---|---|
| Track | Legacy Preview |
| Filename | DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe |
| Size | 183,666,660 bytes (175.16 MiB) |
| SHA-256 | B16ABD84241A1515C15698BE1B21C391AE520E3FFDC4BFCB7FBC93C9A4F92407 |
| Authenticode | NotSigned |
| Updates | Packaged update URL is empty; updates are disabled |
| Source | This repository does not publish the product source for this installer |

Read [verification and SmartScreen guidance](docs/VERIFY_DOWNLOADS.md) before running it.

## Independent verification

Test host: Windows 11 Pro 64-bit, build 26200, x64; 2026-08-15 +08:00.

| Check | Status | Evidence summary |
|---|---|---|
| Exact file, size, SHA-256 | PASS | Exact match |
| Authenticode | NotSigned | No code-signing certificate |
| Microsoft Defender | PASS | 0 threats for the installer and fully extracted tree |
| Gitleaks 8.30.1 | PASS | 0 findings in the extracted tree and app.asar |
| Model / Live2D / Cubism paths | PASS | 0 matches across 33,376 extracted files |
| Installation | PASS | Exit code 0; install directory, desktop/Start shortcuts, and uninstaller created |
| First cold start | FAIL | No loopback service; missing ./machine-id/getMachineId |
| Second cold start | FAIL | Same failure repeated |
| Uninstall | PARTIAL / FAIL | Exit code 0 and process/registry/shortcuts cleared; 17 long-path files remained after 60 seconds |
| Automatic update | DISABLED | resources/update-config.json has an empty URL; no new HarnessDesk updater is connected |

See the [full Legacy Preview notes](docs/LEGACY_PREVIEW_0.1.0-rc.6.md) and [audit manifest](legacy-preview-0.1.0-rc.6.manifest.json).

## Included and excluded

The installer archive contains an Electron client, a bundled Node.js runtime, the Harness runtime closure, and dependencies. The installer supports a selectable destination and creates desktop, Start menu, and uninstall entries.

The following are not verified features of this legacy preview: unified account, SMS, promotional quota, hosted proxy, Hosted BYOK, payments, dynamic Live2D/Cubism, a production update feed, or reproducible source-to-binary builds. Because cold start fails, the UI and core Harness workflows are not verified either.

## Upstream and license

The handoff records associate the package with upstream deepseek-ai/deepseek-harness commit [47f943859bef60e4160492346772ded9b24f765a](https://github.com/deepseek-ai/deepseek-harness/commit/47f943859bef60e4160492346772ded9b24f765a), root package version 0.1.0-rc.5, which is a developer preview. That commit is not the current HarnessDesk candidate, and no upstream product source is published here.

This repository preserves the MIT license, the exact upstream MIT text, and upstream third-party notices. The legacy installer does not place the upstream root LICENSE / THIRD_PARTY_NOTICES at the application root; this Release publishes them as companion assets while clearly retaining that legacy packaging limitation.

## Security reports

Never post keys, cookies, one-time codes, private chats, full logs, or personal data in a public issue. Use [GitHub Private Vulnerability Reporting](https://github.com/HBC-Tech-coder/HarnessDesk/security/advisories/new) for security issues.
