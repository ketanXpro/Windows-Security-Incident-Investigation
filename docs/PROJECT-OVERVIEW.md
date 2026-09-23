# Project Overview

## Windows Security Incident Investigation

### Project Summary

This project documents a Windows security incident investigation
conducted using available Windows Event Logs and Splunk Enterprise.

The investigation focused on reviewing process-creation activity,
searching for selected suspicious execution indicators, documenting
findings, and identifying limitations in the available evidence.

### Objectives

- Review available Windows Security Event ID 4688 records.
- Analyze process activity associated with the reported incident.
- Search for selected suspicious utilities and user-writable paths.
- Document investigation findings and evidence limitations.
- Provide security recommendations based on the investigation.

### Tools and Technologies

- Splunk Enterprise
- Windows Security Event Logs
- Event ID 4688 — Process Creation

### Investigation Scope

The investigation reviewed 429 Event ID 4688 records and documented
the results of selected process-activity and threat-hunting searches.

The investigation was limited by the telemetry available from the
affected endpoint at the time of the incident.

### Key Limitations

- Sysmon was not installed on the affected endpoint during the
  incident.
- Splunk Universal Forwarder was not installed on the affected
  endpoint during the incident.
- The available records did not conclusively establish the
  execution chain behind the reported WhatsApp forwarding.
- The SOC did not independently identify the malware family.

### Project Deliverables

- Security Incident Investigation Report
- Incident Timeline
- Investigation Searches
- Findings and Limitations
- Security Recommendations

### Disclaimer

This repository documents an investigation case study based on
the evidence available to the SOC. Findings are limited to the
records reviewed and should not be interpreted as a complete
forensic reconstruction of the incident.

### Documentation

- [Incident Timeline](INCIDENT-TIMELINE.md)
- [Investigation Searches](INVESTIGATION-SEARCHES.md)
- [Findings and Limitations](FINDINGS-AND-LIMITATIONS.md)
- [Security Recommendations](SECURITY-RECOMMENDATIONS.md)
- [Investigation Report](SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
