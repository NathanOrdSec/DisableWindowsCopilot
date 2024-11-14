# DisableWindowsCopilot
You can download the .reg files and run them from wherever to disable (DownedPilot) and re-enable (RevivePilot) Copilot on Windows.

Alternatively, drop these commands to enable or disable Windows Copilot into an Administrator PowerShell window. You may have to click Copilot for it to yeet itself. 
## Disable Windows Copilot
```
reg add HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```

## Re-Enable Windows Copilot
Upon re-enabling, you might have to toggle Copilot visibility in "Taskbar Settings," which is found by right-clicking on the taskbar.
```
reg delete HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot /f
```

## Run Box One-Liners!
Paste into Run Menu (Windows Key+R) and hit Control+Shift+Enter, then accept UAC prompt
### Disable
```
powershell -W H -NOP -NONI reg add HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 1
```
### Re-Enable
Yes, setting the value to 0 works just as well as deleting the key outright! 
```
powershell -W H -NOP -NONI reg add HKLM\Software\Policies\Microsoft\Windows\WindowsCopilot /v "TurnOffWindowsCopilot" /t REG_DWORD /f /d 0
```
