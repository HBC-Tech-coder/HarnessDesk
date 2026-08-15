# Verify downloads and SmartScreen / 下载校验与 SmartScreen

## 中文

此旧包没有 Authenticode 代码签名，Windows 可能显示“未知发布者”。SHA-256 只能证明下载字节是否与本仓公布的文件一致，不能证明发布者身份，也不能修复已知冷启动故障。

在 PowerShell 中进入下载目录后运行：

    Get-FileHash -Algorithm SHA256 -LiteralPath '.\DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe'
    Get-AuthenticodeSignature -LiteralPath '.\DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe' |
      Select-Object Status, StatusMessage

预期：

- SHA-256 必须精确等于 B16ABD84241A1515C15698BE1B21C391AE520E3FFDC4BFCB7FBC93C9A4F92407
- 签名状态必须显示 NotSigned
- 文件大小必须是 183,666,660 bytes

任一项不一致都不要运行。不要关闭 SmartScreen、不要修改系统安全策略，也不要使用绕过命令。即使三项一致，本版本仍已知连续两次冷启动失败，只适合归档和问题复现。

## English

This legacy package has no Authenticode signature, so Windows may show “Unknown publisher.” SHA-256 proves only that the downloaded bytes match the published asset. It does not establish publisher identity and does not fix the known cold-start failure.

From PowerShell in the download directory:

    Get-FileHash -Algorithm SHA256 -LiteralPath '.\DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe'
    Get-AuthenticodeSignature -LiteralPath '.\DeepSeek-Harness-Setup-0.1.0-rc.6-x64.exe' |
      Select-Object Status, StatusMessage

Expected:

- SHA-256 exactly B16ABD84241A1515C15698BE1B21C391AE520E3FFDC4BFCB7FBC93C9A4F92407
- signature status NotSigned
- size 183,666,660 bytes

Do not run the file if any value differs. Do not disable SmartScreen or weaken system policy. Even with matching values, this build failed two independent cold starts and is intended only for archival testing and issue reproduction.
