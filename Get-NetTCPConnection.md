```Bash
#要列出本機開啟的埠口 (open ports)
Get-NetTCPConnection -State Listen
#若要在 Windows 防火牆中打開特定的埠口 (port)
New-NetFirewallRule -DisplayName "Open TCP Port 8080" -Direction Inbound -Protocol TCP -LocalPort 8080 -Action Allow
#檢查是否有建立成功
Get-NetFirewallRule -DisplayName "Open TCP Port 8080"
#注意這時候用 Get-NetTCPConnection -State Listen 是看不到的，除非有服務正在使用8080
```
