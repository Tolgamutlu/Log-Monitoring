# Atomic Red Team Tests Used

Follow the following installation guide first to get started before executing the powershell commands:

https://github.com/redcanaryco/invoke-atomicredteam/wiki/Execute-Atomic-Tests-(Local)


## T1059.001 - PowerShell Encoded Command

```powershell
Invoke-AtomicTest T1059.001 -TestNumbers 17
```

Expected detection:

- Suspicious PowerShell execution
- Encoded command usage
- Rule ID 100100

Cleanup:

```powershell
Invoke-AtomicTest T1059.001 -TestNumbers 17 -Cleanup
```

## T1053.005 - Scheduled Task

```powershell
Invoke-AtomicTest T1053.005 -TestNumbers 2
```

Expected detection:

- Scheduled task creation
- Use of task scheduling utilities
- Rule ID 100101

Cleanup:

```powershell
Invoke-AtomicTest T1053.005 -TestNumbers 2 -Cleanup
```

## T1136.001 - Local Account

```powershell
Invoke-AtomicTest T1136.001 -TestNumbers 4
```

Expected detection:

- Local user account creation
- Account-related Windows event data
- Rule ID 100102

Cleanup:

```powershell
Invoke-AtomicTest T1136.001 -TestNumbers 4 -Cleanup
```

## T1543.003 - Windows Service

```powershell
Invoke-AtomicTest T1543.003 -TestNumbers 1
```

Expected detection:

- Windows service creation or modification
- Service-related event data
- Rule ID 100103

Cleanup:

```powershell
Invoke-AtomicTest T1543.003 -TestNumbers 1 -Cleanup
```
