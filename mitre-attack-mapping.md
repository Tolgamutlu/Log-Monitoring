# MITRE ATT&CK Mapping

This lab mapped each custom detection to a relevant MITRE ATT&CK technique to make the alerts easier to understand from an attacker behaviour perspective.

## Detection 1: Suspicious PowerShell Encoded Command

- **Technique:** T1059.001
- **Name:** Command and Scripting Interpreter: PowerShell
- **Reason for Mapping:** PowerShell is a legitimate Windows administration tool, but attackers may abuse it to execute commands, run scripts, download payloads, or execute encoded commands.

## Detection 2: Scheduled Task Persistence

- **Technique:** T1053.005
- **Name:** Scheduled Task/Job: Scheduled Task
- **Reason for Mapping:** Scheduled tasks can be used to execute commands at logon, startup, or a specific time. This may support persistence.

## Detection 3: Local User Account Creation

- **Technique:** T1136.001
- **Name:** Create Account: Local Account
- **Reason for Mapping:** Attackers may create local accounts to maintain access to a compromised system.

## Detection 4: Windows Service Creation or Modification

- **Technique:** T1543.003
- **Name:** Create or Modify System Process: Windows Service
- **Reason for Mapping:** Windows services can be abused to run code in the background, maintain persistence, or execute with elevated privileges.

## Why MITRE Mapping Helped

Mapping the alerts to MITRE ATT&CK helped me understand the behaviour behind the alert rather than treating it as just a log entry. It also made the detections easier to explain in a SOC-style investigation.