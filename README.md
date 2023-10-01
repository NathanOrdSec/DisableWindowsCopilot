# DisableWindowsCopilot
Drop these commands to enable or disable Windows Copilot into a Administrator PowerShell window.
## Disable Windows Copilot
```
reg add HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```

## Re-Enable Windows Copilot
Upon re-enabling, you might have to go toggle Copilot visibility in "Taskbar Settings" which is found by right-clicking on the taskbar.
```
reg delete HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /f
```

## One-Liners!
Paste into Run Menu (Windows Key+R) and hit Control+Shift+Enter, then accept UAC prompt
### Disable
```
powershell -W H -NOP -NONI reg add HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```
### Re-Enable
```
powershell -W H -NOP -NONI reg add HKCU\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 0
```
