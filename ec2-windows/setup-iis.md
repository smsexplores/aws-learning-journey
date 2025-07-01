\# Installing IIS on Windows Server



Run these PowerShell commands on your EC2 Windows instance to install IIS:



```powershell

Install-WindowsFeature -name Web-Server -IncludeManagementTools



