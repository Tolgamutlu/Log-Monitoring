# Windows SIEM Detection Lab: Wazuh, Sysmon and MITRE ATT&CK

This repository supports my Windows SIEM detection lab using **Wazuh**, **Sysmon**, **Windows Event Logs**, and **Atomic Red Team**.

The purpose of this project was to build a small SOC-style lab environment, generate controlled suspicious endpoint activity, create custom Wazuh detection rules, map alerts to MITRE ATT&CK techniques, and document the investigation process.

## Project Summary

In this lab, I was able to:

- Built a Wazuh SIEM environment using an Ubuntu virtual machine.
- Deployed the Wazuh agent to a Windows endpoint.
- Installed Sysmon to collect detailed endpoint telemetry.
- Used Atomic Red Team to safely simulate selected MITRE ATT&CK techniques.
- Created custom Wazuh rules for suspicious Windows endpoint behaviour.
- Reviewed alert fields such as host, user, process, command line, timestamp, parent process, and MITRE mapping.
- Documented possible false positives and recommended analyst response actions.

## Detection Coverage

| Rule ID | Detection | MITRE ATT&CK Technique | Main Log Source |
|---|---|---|---|
| 100100 | Suspicious PowerShell encoded command | T1059.001 - PowerShell | Sysmon / Windows Event Logs |
| 100101 | Scheduled task persistence | T1053.005 - Scheduled Task | Sysmon / Windows Security Logs |
| 100102 | Local user account creation | T1136.001 - Local Account | Windows Security Logs / Sysmon |
| 100103 | Windows service creation or modification | T1543.003 - Windows Service | Windows System Logs / Sysmon |

## Important Note

The rules in this repository were created for a controlled lab environment. They are designed to demonstrate detection logic and analyst thinking. In a production environment, they would need further testing, tuning, severity adjustment, and false-positive review.

## Skills Demonstrated

- SIEM monitoring
- Windows endpoint logging
- Sysmon event analysis
- Wazuh custom rule creation
- MITRE ATT&CK mapping
- Alert triage
- False-positive review
- SOC-style documentation
- Basic incident response thinking