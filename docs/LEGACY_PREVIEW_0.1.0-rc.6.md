# Legacy Preview 0.1.0-rc.6 — unsigned / known cold-start failure

> **旧版预览 / Legacy Preview**
>
> This is not the current HarnessDesk release candidate, not a production release, and not recommended for daily use.
>
> 这不是当前 HarnessDesk 候选，不是正式版，也不建议日常使用。

## Identity / 身份说明

HarnessDesk is an independent, unofficial community client. It is not affiliated with, authorized by, sponsored by, or endorsed by DeepSeek AI. The legacy installer retains a historical filename and embedded product metadata that say “DeepSeek Harness”; those strings identify old artifact metadata and upstream compatibility, not the HarnessDesk product brand.

HarnessDesk 是独立、非官方的社区客户端，与 DeepSeek AI 无隶属、授权、赞助或官方背书关系。旧安装包保留历史文件名与内嵌名称，这些字符串只用于识别旧资产和上游兼容性，不是 HarnessDesk 产品商标。

## Asset / 资产

| Field / 字段 | Value / 值 |
|---|---|
| Filename / 文件名 | DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe |
| Bytes / 字节 | 183,666,660 |
| MiB | 175.16 |
| SHA-256 | B16ABD84241A1515C15698BE1B21C391AE520E3FFDC4BFCB7FBC93C9A4F92407 |
| Authenticode | NotSigned |
| Release type | Prerelease, not latest |
| Product source | Not published |

## Mechanical verification / 机械核验

Audit host: Windows 11 Pro 64-bit, build 26200, x64. Audit time: 2026-08-15 +08:00.

| Gate | Result | Evidence |
|---|---|---|
| Exact file identity | PASS | Filename, 183,666,660 bytes, and SHA-256 matched |
| Authenticode | NotSigned | No signing certificate |
| Microsoft Defender | PASS | 0 threats on the installer and 33,376-file extracted tree |
| Gitleaks 8.30.1 | PASS | 0 findings on extracted tree and app.asar |
| Reparse points after extraction | PASS | 0 |
| Model / Live2D / Cubism paths | PASS | 0 |
| Packaged update configuration | DISABLED | resources/update-config.json contains an empty URL |
| Silent installation | PASS | Exit code 0; 33,225 installed files; desktop/Start shortcuts and uninstaller created |
| First cold start | FAIL | No loopback listener; missing ./machine-id/getMachineId |
| Second cold start | FAIL | Same error repeated |
| Process cleanup after failed launch | PASS WITH FORCE | Exact package process tree was terminated; no package process remained |
| Silent uninstall | PARTIAL / FAIL | Exit code 0; registry and shortcuts removed; 17 long-path files remained after 60 seconds |
| UI and core Harness workflows | UNVERIFIED | Cold start did not complete |
| Multi-version Windows compatibility | UNVERIFIED | One Windows 11 x64 host tested |
| Reproducible source-to-binary build | UNVERIFIED | Product source is not published in this release |
| Full dependency/legal closure in installer | UNVERIFIED / LEGACY LIMITATION | Companion notices are published; upstream root notices are absent from the installed app root |

## Packaged components / 包含组件

Archive inspection confirms an Electron client, bundled Node.js, Harness runtime closure, and runtime dependencies. The installer supports a selectable destination and creates desktop, Start menu, and uninstall entries.

Because startup fails, these packaging facts must not be presented as proof that the application is usable.

## Not available or not verified / 未上线或未验证

- HarnessDesk unified account or SMS login
- promotional quota or consumable credits
- hosted provider proxy or Hosted BYOK
- payments or recharge
- dynamic Live2D/Cubism
- production update feed
- new HarnessDesk Ed25519 trust root
- successful UI, agent, terminal, or model workflow

## Update behavior / 更新行为

The legacy binary contains updater code, but its bundled URL is empty. Automatic updates are therefore disabled. No new HarnessDesk key, signed feed, or updater channel is published with this release, and future updaters must not target this legacy asset.

旧包包含更新器代码，但内置 URL 为空，因此自动更新关闭。本 Release 不发布新的 HarnessDesk key、签名 feed 或更新通道，未来更新器也不得指向此旧资产。

## SmartScreen / Windows 提示

Windows may display “Unknown publisher.” Verify SHA-256 before making any decision. Do not disable SmartScreen or weaken Windows security policy. Matching the hash does not make the build signed or repair the known startup failure.

## License / 许可

The Release publishes LICENSE, LICENSES/DeepSeek-Harness-MIT.txt, and THIRD_PARTY_NOTICES.md as companion assets. The old installer lacks the upstream root LICENSE / THIRD_PARTY_NOTICES at the installed app root; that limitation is disclosed rather than treated as a passed current release gate.
