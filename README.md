# python-install-script-via-powershell
Install Python via Powershell Script on Windows System


Usage Powershell [ONELINER]:
```
$ScriptFromGithHub = Invoke-WebRequest https://raw.githubusercontent.com/korlersorter/python-install-script-via-powershell/main/install.ps1 -UseBasicParsing; Invoke-Expression $($ScriptFromGithHub.Content);
```

Usage BATCH Script:
```
@echo off

if not "%1"=="am_admin" (

    powershell -Command "Start-Process -Verb RunAs -FilePath '%0' -ArgumentList 'am_admin'"
    
    exit /b
    
)

start cmd /k powershell.exe $ScriptFromGithHub = Invoke-WebRequest https://raw.githubusercontent.com/korlersorter/python-install-script-via-powershell/main/install.ps1 -UseBasicParsing; Invoke-Expression $($ScriptFromGithHub.Content);

```


