
Guide based on: https://www.saotn.org/how-do-i-get-my-yubikey-to-work-with-ssh-in-windows-11-and-windows-10/

## Remove OpenSSH
Open an elevated PowerShell window
```
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
Remove-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0
```

## Download OpenSSH for Windows

https://github.com/PowerShell/Win32-OpenSSH/releases

## Install OpenSSH client
The OpenSSH .msi Windows Installer file by default installs both ssh Server and Client. We only want to install the client, the command line option is ADDLOCAL=Client. By default, msiexec.exe doesn’t add the installation path to your system’s $env:path environment variable. For this, add ADD_PATH=1 to the command. This makes the full command to install OpenSSH Client on your system:
Execute in an elevated PowerShell window
```
Start-Process -NoNewWindow msiexec.exe  -ArgumentList "/i <full path to msi installer> ADDLOCAL=Client ADD_PATH=1" -Wait
```
