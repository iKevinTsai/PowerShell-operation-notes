Get-WmiObject 是 PowerShell 中用來取得 Windows Management Instrumentation (WMI) 物件的指令。WMI 是一個 Windows 管理框架，它提供了一種標準方法來收集 Windows 系統資訊，例如硬體、軟體、網路等等的訊息。
使用 Get-WmiObject 指令，您可以瀏覽 WMI 名稱空間、類別及其屬性，並從中擷取資訊。例如，以下是一個使用 Get-WmiObject 指令取得電腦系統資訊的範例：
```Bash
#這個指令會返回一個包含電腦系統資訊的 WMI 物件，例如系統名稱、製造商、型號、作業系統等等。
Get-WmiObject -Class Win32_ComputerSystem
#您可以使用 Select-Object 指令來篩選和顯示這些屬性
Get-WmiObject -Class Win32_ComputerSystem | Select-Object Name, Manufacturer, Model, OperatingSystem
#您也可以使用 Where-Object 指令來篩選 WMI 物件：顯示具有 4 個或更多核心的處理器
Get-WmiObject -Class Win32_Processor | Where-Object { $_.NumberOfCores -ge 4 }
```
Win32_LogicalDisk 是 WMI 中的一個類別，它代表系統中的邏輯磁碟。
```Bash
#使用 Get-WmiObject 取得系統中邏輯磁碟資訊
Get-WmiObject -Class Win32_LogicalDisk | Select-Object DeviceID, VolumeName, FileSystem, Size, FreeSpace
```
