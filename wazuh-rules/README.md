# Wazuh Custom Rules

This folder contains lab-focused Wazuh custom rules for the Windows SIEM detection project.

## Rules Included

| File | Rule ID | Detection |
|---|---|---|
| `100100_powershell_encoded_command.xml` | 100100 | Suspicious PowerShell encoded command |
| `100101_scheduled_task_persistence.xml` | 100101 | Scheduled task persistence |
| `100102_local_user_creation.xml` | 100102 | Local user account creation |
| `100103_windows_service_modification.xml` | 100103 | Windows service creation or modification |
| `local_rules_combined.xml` | 100100-100103 | All custom rules in one file |

## Deployment Note

These rules are intended for lab demonstration and may require field-name tuning depending on the Wazuh version, Sysmon configuration, and Windows log source.

A common location for custom Wazuh rules is:

```text
/var/ossec/etc/rules/local_rules.xml
```

After changing Wazuh rules, restart the Wazuh manager:

```bash
sudo systemctl restart wazuh-manager
```

## Important

Test custom rules in a lab before using them in production. Production rules should be tuned to reduce false positives and validated against expected business activity.
