
Guide based on: https://www.saotn.org/how-do-i-get-my-yubikey-to-work-with-ssh-in-windows-11-and-windows-10/

## Remove OpenSSH
Open an elevated PowerShell window
```
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
Remove-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0
```
