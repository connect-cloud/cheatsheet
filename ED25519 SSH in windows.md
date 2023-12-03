## Remove OpenSSH
Open an elevated PowerShell window
```
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
Remove-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0
```
