# Case Summary

## Windows Security Incident Investigation

### 1. Case Overview

This case study documents a Windows security incident involving
a suspicious ZIP file received through WhatsApp and subsequently
reported unauthorized forwarding of the same file.

The SOC reviewed available Windows Security Event Logs using
Splunk Enterprise to examine process activity and search for
selected suspicious indicators.

### 2. Incident Summary

- A ZIP file was received through WhatsApp from an unknown
  third party and appeared to contain a video.
- The file was interacted with on three computers.
- Two computers could not play the file.
- The primary Windows endpoint was the computer on which the
  file was opened or interacted with.
- On 11 September 2026, the same ZIP file was reportedly
  forwarded from the company's WhatsApp session without
  the user's intention.
- The VAPT/Bug-Bounty team classified the artifact as a Trojan.
  The SOC did not independently identify its malware family.

### 3. Investigation Performed

The SOC:

- Collected available Windows Event Log evidence.
- Imported the evidence into Splunk Enterprise.
- Analyzed 429 Windows Security Event ID 4688 records.
- Reviewed available process activity for 9 and 11 September 2026.
- Searched for selected suspicious utilities and user-writable
  paths.
- Documented findings, limitations, and recommendations.

### 4. Key Findings

- No suspicious process names were identified in the reviewed
  Event ID 4688 process activity.
- Searches for selected LOLBins and user-writable paths returned
  no matches in the available dataset.
- The imported dataset did not contain populated
  `Process_Command_Line` values.

### 5. Evidence Limitations

- Sysmon and Splunk Universal Forwarder were not installed on
  the affected endpoint at the time of the incident.
- The available process-creation records provided limited
  historical visibility.
- The evidence did not conclusively establish whether the ZIP
  file executed malicious code.
- The evidence did not establish a process-level link between
  the ZIP file and the reported WhatsApp forwarding.

### 6. Conclusion

The SOC documented the available process-creation evidence,
the results of the reviewed searches, and the limitations
affecting the investigation.

The precise execution chain and mechanism behind the reported
WhatsApp forwarding were not conclusively established from
the available evidence.

### 7. Project Deliverables

- [Project Overview](PROJECT-OVERVIEW.md)
- [Incident Timeline](INCIDENT-TIMELINE.md)
- [Investigation Methodology](METHODOLOGY.md)
- [Investigation Searches](INVESTIGATION-SEARCHES.md)
- [Findings and Limitations](FINDINGS-AND-LIMITATIONS.md)
- [Security Recommendations](SECURITY-RECOMMENDATIONS.md)
- [Full Investigation Report](SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
