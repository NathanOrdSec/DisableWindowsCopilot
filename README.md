# DisableWindowsCopilot
Drop these commands to enable or disable Windows Copilot into a Administrator PowerShell window.
## Disable Windows Copilot
```
reg add HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```

## Re-Enable Windows Copilot
```
reg delete HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /f
```
