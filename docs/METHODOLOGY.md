# Investigation Methodology

## 1. Overview

This document describes the investigation approach used in the
Windows security incident case study.

The investigation focused on reviewing available Windows Security
Event Logs in Splunk Enterprise, examining process-creation activity,
documenting search results, and identifying evidence limitations.

## 2. Investigation Workflow

### Step 1: Evidence Collection

Windows Event Log evidence was collected for analysis.

The investigation was limited to the evidence made available to
the SOC. Sysmon and Splunk Universal Forwarder were not installed
on the affected endpoint at the time of the incident.

### Step 2: Evidence Extraction and Review

The collected Windows Security Event Log data was imported into
Splunk Enterprise for review.

The investigation focused on Event ID 4688, which records
process-creation activity when the relevant auditing is configured.

### Step 3: Process Activity Analysis

A total of 429 Event ID 4688 records were analyzed.

The reviewed process activity included records associated with
9 September and 11 September 2026.

The SOC examined the available process information and looked
for suspicious process names and unexpected activity.

### Step 4: Threat-Hunting Searches

The investigation included searches for selected Living-off-the-Land
Binaries (LOLBins) and selected user-writable paths.

No matches were returned by those searches in the available dataset.

The imported dataset did not contain populated
`Process_Command_Line` values.

### Step 5: Findings and Limitations

The SOC documented the observed results and the limitations of
the available telemetry.

The absence of suspicious process names or search matches was
not treated as proof that the endpoint was uncompromised.

### Step 6: Reporting and Recommendations

The investigation findings, evidence limitations, and security
recommendations were documented in the Security Incident
Investigation Report.

## 3. Tools and Data Sources

- Splunk Enterprise
- Windows Security Event Logs
- Event ID 4688 — Process Creation

## 4. Methodology Limitations

The available evidence did not conclusively establish:

- Whether the ZIP file executed malicious code.
- The exact execution chain associated with the incident.
- A process-level connection between the ZIP file and the
  reported WhatsApp forwarding.
- The malware family involved.

The VAPT/Bug-Bounty team's Trojan classification is reported
as a separate team's assessment; it was not an independent
malware-family identification by the SOC.

## 5. Conclusion

The methodology provided a structured review of the available
process-creation evidence and documented the limits of the
investigation.

The results should be understood within the scope of the
evidence that was available and reviewed.

## Related Documentation

- [Project Overview](PROJECT-OVERVIEW.md)
- [Incident Timeline](INCIDENT-TIMELINE.md)
- [Investigation Searches](INVESTIGATION-SEARCHES.md)
- [Findings and Limitations](FINDINGS-AND-LIMITATIONS.md)
- [Security Recommendations](SECURITY-RECOMMENDATIONS.md)
- [Investigation Report](SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
