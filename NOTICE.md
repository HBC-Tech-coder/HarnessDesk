# HarnessDesk notices

## Product identity

HarnessDesk is an independent, unofficial community client. It is not affiliated with, authorized by, sponsored by, or endorsed by DeepSeek AI. DeepSeek and DeepSeek Harness identify the compatible upstream open-source project only.

The Legacy Preview installer retains historical filename and embedded product metadata that say “DeepSeek Harness.” Those strings are legacy artifact metadata, not the HarnessDesk product name and not a claim of official status.

## Upstream origin

The Legacy Preview handoff records identify this upstream baseline:

- Repository: https://github.com/deepseek-ai/deepseek-harness
- Commit: 47f943859bef60e4160492346772ded9b24f765a
- Root package version: 0.1.0-rc.5
- License: MIT
- Upstream copyright: Copyright (c) 2026 DeepSeek

The exact upstream MIT text is preserved at LICENSES/DeepSeek-Harness-MIT.txt.

## Legacy packaging limitation

The old installer contains Electron/Chromium and Node license material plus many package-level license files, but it does not place the upstream root LICENSE or THIRD_PARTY_NOTICES at the installed application root. The GitHub Release therefore publishes LICENSE, LICENSES/DeepSeek-Harness-MIT.txt, and THIRD_PARTY_NOTICES.md as companion assets.

This companion publication improves notice availability but does not represent that the old binary has passed the current HarnessDesk legal or release-candidate gate. Future candidates must include the complete shipped-license closure inside the distribution itself.

## Trademarks

All trademarks and project names belong to their respective owners. The MIT license grants software rights; it does not grant trademark rights or official endorsement.
