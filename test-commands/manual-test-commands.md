# Manual Test Commands

These are example manual commands that can generate similar lab activity for testing. Use only in an authorised lab environment.

## PowerShell Encoded Command Example

```powershell
powershell.exe -Execution Bypass -Command "Write-Output test"
```

## Scheduled Task Creation Example

```powershell
schtasks /create /tn "LabTaskTest" /tr "cmd.exe /c echo test" /sc once /st 23:59
```

Cleanup:

```powershell
schtasks /delete /tn "LabTaskTest" /f
```

## Local User Account Creation Example

```powershell
net user labtestuser P@ssw0rd123 /add
```

Cleanup:

```powershell
net user labtestuser /delete
```

## Windows Service Creation Example

```powershell
sc.exe create LabServiceTest binPath= "C:\Windows\System32\cmd.exe /c echo test" start= demand
```

Cleanup:

```powershell
sc.exe delete LabServiceTest
```

## Note

These manual commands are included to show what behaviours the detections are intended to identify. Atomic Red Team was used in the main lab because it provides controlled ATT&CK-mapped tests and cleanup options.
