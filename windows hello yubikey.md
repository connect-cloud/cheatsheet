
## Enable security key logon on windows
- Open the Registry Editor (regedit.exe)
- Navigate to the following registry location:HKLM\SOFTWARE\Microsoft\Policies\PassportForWork\SecurityKey
- If the PassportForWork and SecurityKey registry keys don't exist, create them.
- Create a new DWORD (32-bit) value, named UseSecurityKeyForSignIn.
- Provide 1 as the data for the new value.
