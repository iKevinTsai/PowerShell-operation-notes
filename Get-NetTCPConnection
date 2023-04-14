```Bash
#要列出本機開啟的埠口 (open ports)
Get-NetTCPConnection -State Listen
#若要在 Windows 防火牆中打開特定的埠口 (port)
New-NetFirewallRule -DisplayName "Open TCP Port 8080" -Direction Inbound -Protocol TCP -LocalPort 8080 -Action Allow
```
