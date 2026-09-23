# Tools and Technologies

## Windows Security Incident Investigation

## 1. Overview

This document lists the tools and data sources used during the
investigation, along with their roles in the documented analysis.

## 2. Tools Used

### Splunk Enterprise

**Purpose:** Security log analysis.

Used to import and review the available Windows Event Log evidence,
analyze Event ID 4688 process-creation records, and conduct searches
for selected suspicious indicators.

### Windows Security Event Logs

**Purpose:** Endpoint process-creation evidence.

Event ID 4688 records were reviewed to examine available process
activity associated with the incident.

## 3. Data Source

| Data Source | Description |
|---|---|
| Windows Security Event ID 4688 | Process-creation records analyzed during the investigation |

## 4. Telemetry Limitations

The following tools were not installed on the affected endpoint
at the time of the incident:

- Sysmon
- Splunk Universal Forwarder

Their absence limited the endpoint telemetry available for
historical investigation.

## 5. Scope Note

This document describes tools and data sources relevant to the
reported investigation. It does not claim that additional tools
or telemetry sources were deployed or used.

## Related Documentation

- [Project Overview](PROJECT-OVERVIEW.md)
- [Case Summary](CASE-SUMMARY.md)
- [Investigation Methodology](METHODOLOGY.md)
- [Investigation Searches](INVESTIGATION-SEARCHES.md)
- [Findings and Limitations](FINDINGS-AND-LIMITATIONS.md)
- [Security Recommendations](SECURITY-RECOMMENDATIONS.md)
- [Full Investigation Report](SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
