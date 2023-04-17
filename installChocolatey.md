```Bash
Get-ExecutionPolicy
# 如果顯示 Ristricted，則再執行以下指令
Set-ExecutionPolicy AllSigned
# 按下 y 繼續
# 安裝 chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
# 確認是否安裝完成
choco
```
