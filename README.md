# DisableWindowsCopilot
Drop these commands to enable or disable Windows Copilot into a Administrator PowerShell window.
## Disable Windows Copilot
```
New-Item -Path HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot -Force
reg add HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```

## Re-Enable Windows Copilot
```
Remove-Item -Path HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot -Force
reg delete HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot
```
