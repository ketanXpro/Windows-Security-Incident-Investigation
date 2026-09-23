# Windows Security Incident Investigation

A cybersecurity incident investigation case study documenting suspected Trojan-related activity involving a Windows endpoint at **Cybugs**. The investigation reviewed available Windows Security Event ID 4688 process-creation records using Splunk Enterprise and documented the findings, limitations, and recommendations.

---

## 📑 Contents

- [Investigation Report](docs/SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
- [Evidence Screenshots](evidence/screenshots/README.md)

---

## 🚨 Incident Overview

A suspicious ZIP archive received through WhatsApp appeared to contain a video. The file was interacted with on three computers. On **11 September 2026**, the same ZIP file was observed being sent through the company's WhatsApp session to other contacts without intentional user action.

A separate VAPT/Bug-Bounty assessment classified the artifact as a Trojan. That classification is attributed to the separate assessment; this case study does not independently identify a malware family or establish the precise execution mechanism.

---

## 🎯 Investigation Scope

The investigation focused on the available Windows Security Event ID 4688 process-creation data. The records were analyzed using Splunk Enterprise to review process activity and search for potentially suspicious execution.

Activities included:

- Reviewing process names and available parent-child relationships.
- Reviewing process activity around 9 and 11 September 2026.
- Searching for selected commonly abused Windows utilities (LOLBins).
- Searching selected user-writable paths for process execution.
- Checking whether process command-line values were populated.
- Assessing what the available telemetry could and could not establish.

---

## 🔍 Key Findings

- The available dataset contained **429 Event ID 4688 records**.
- The reviewed process activity primarily showed standard Windows system processes and expected parent-child relationships.
- No suspicious process name was identified in the reviewed records for 9 or 11 September 2026.
- Searches for selected LOLBins and selected user-writable paths returned no matching events.
- No populated `Process_Command_Line` values were available in the imported dataset.

> These findings apply only to the available dataset and searches. They do not prove that the endpoint was free of malicious activity.

---

## ⚠️ Investigation Limitations

Sysmon and Splunk Universal Forwarder were not installed on the affected endpoint at the time of the incident. The investigation therefore relied primarily on the available Event ID 4688 evidence.

The available data did not conclusively establish whether the suspicious artifact executed or establish a direct causal link between a specific process and the WhatsApp forwarding behavior.

---

## 🛡️ Recommendations

The report recommends improving:

- Endpoint protection and security configuration review.
- Endpoint telemetry and centralized log monitoring.
- Detection rules and alerting.
- Security awareness and incident-response procedures.
- Change control for production security configuration changes.

Recommendations should be evaluated against the organization's approved security architecture and operational requirements.

---

## 🧰 Tools and Technologies

- Splunk Enterprise
- Windows Security Event Logs
- Windows Security Event ID 4688
- Structured JSON event data

---

## 📂 Repository Structure

```text
Windows-Security-Incident-Investigation/
├── README.md
├── docs/
│   ├── REPORT-REDACTION-NOTE.md
│   └── SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf
└── evidence/
    └── screenshots/
        └── README.md
