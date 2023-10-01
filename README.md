# DisableWindowsCopilot

## Disable Windows Copilot
```
New-Item -Path HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot -Force
reg add HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```

## Re-Enable Windows Copilot
```
Remove-Item -Path HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot -Force
reg delete HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot
```
