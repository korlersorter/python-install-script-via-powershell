# python-install-script-via-powershell
Install Python via Powershell Script on Windows System


Usage Powershell [ONELINER] [METHOD 1]:
```
$ScriptFromGithHub = Invoke-WebRequest https://github.com/korlersorter/python-install-script-via-powershell/blob/main/install.ps1 -UseBasicParsing; Invoke-Expression $($ScriptFromGithHub.Content);
```

[METHOD 2]
```
$ScriptFromGithHub = Invoke-RestMethod https://github.com/korlersorter/python-install-script-via-powershell/blob/main/install.ps1 -Method Get; Invoke-Expression $($ScriptFromGithHub.Content);
```

Usage BATCH Script:
```
@echo off

if not "%1"=="am_admin" (

    powershell -Command "Start-Process -Verb RunAs -FilePath '%0' -ArgumentList 'am_admin'"
    
    exit /b
    
)

SET var=%cd%

ECHO %var%

start cmd /k powershell.exe $ScriptFromGithHub = Invoke-WebRequest https://github.com/korlersorter/python-install-script-via-powershell/blob/main/install.ps1 -UseBasicParsing; Invoke-Expression $($ScriptFromGithHub.Content);

pause
```


