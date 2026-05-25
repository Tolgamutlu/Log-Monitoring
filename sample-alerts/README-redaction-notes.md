# Redacted Wazuh Alert Samples

These files have been modified by AI to be both prettified and redact any sensitive information from the four original Wazuh alerts.

Redactions applied:
- Personal usernames and Windows profile paths were replaced with generic lab values.
- Hostnames, local domain names, manager names, and private IP addresses were replaced with lab/test placeholders.
- Machine-specific SIDs, process GUIDs, logon GUIDs, logon IDs, alert IDs, and Windows event record IDs were redacted or normalized.
- PowerShell temp script names and binary hashes were redacted.
- MITRE ATT&CK IDs, rule IDs, event IDs, provider names, channels, rule descriptions, and detection-relevant command context were preserved where safe.

Note:
- The `full_log` field is still stored as an escaped JSON string to preserve the original Wazuh alert schema, but the contents inside it have also been redacted.
