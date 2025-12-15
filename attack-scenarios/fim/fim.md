# File Integrity Monitoring (FIM)

In this project, File Integrity Monitoring was used to detect unauthorized
changes on the victim system.

Sensitive system files were monitored in order to detect file creation,
modification or deletion.

When a file was created or modified, the event was recorded and analyzed
by Wazuh.

An alert was then generated and displayed on the Wazuh dashboard.

This scenario shows how a SOC can detect suspicious system changes that
may indicate malware activity or unauthorized access.
