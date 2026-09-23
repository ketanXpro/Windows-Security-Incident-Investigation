# Windows Security Incident Investigation

A sanitized case study documenting a suspected malware-related incident involving a Windows endpoint at **Cybugs**. The investigation reviewed available Windows Security Event ID 4688 process-creation data in Splunk Enterprise and records the findings, limitations, and recommendations supported by that evidence.

> **Publication status:** This repository is a working portfolio draft. Do not publish client-identifying information, raw event logs, screenshots containing hostnames or user data, or the original report marked confidential. Add only an approved, sanitized report and evidence.

## Incident summary

A suspicious ZIP archive received through WhatsApp appeared to contain a video. The artifact was interacted with on three computers. On 11 September 2026, the same ZIP was observed being sent through the company's WhatsApp session to other contacts without intentional user action.

A separate VAPT/Bug-Bounty assessment classified the artifact as a Trojan. This classification is attributed to that separate assessment; this SOC case study does not independently identify a malware family or establish the execution mechanism.

## Investigation scope

- Review available Windows Security Event ID 4688 process-creation events.
- Analyze the exported event data using Splunk Enterprise.
- Review process names and available parent-child relationships.
- Search for selected commonly abused Windows utilities (LOLBins).
- Search for process execution from selected user-writable paths.
- Review activity around 9 and 11 September 2026.
- Document evidence-based findings, limitations, and recommendations.

## Key findings

- The available dataset contained 429 Event ID 4688 records.
- The reviewed process activity primarily showed standard Windows system processes and expected parent-child relationships.
- No suspicious process name was identified in the reviewed records for 9 or 11 September 2026.
- Searches for selected LOLBins and selected user-writable paths returned no matching events.
- The imported dataset had no populated process command-line values.

These results describe only the available dataset and searches; they do not prove that the endpoint was free of malicious activity.

## Limitations

Sysmon and Splunk Universal Forwarder were not installed on the affected endpoint at the time of the incident. The investigation therefore relied primarily on the available Event ID 4688 evidence. The available telemetry does not conclusively establish whether the suspicious artifact executed or prove a direct causal link between a process and the WhatsApp forwarding behavior.

## Recommendations

Recommendations documented in the investigation include maintaining endpoint security protections, reviewing Windows Security configuration, improving endpoint telemetry and centralized log monitoring, maintaining relevant detections and alerting, strengthening security awareness and incident-response procedures, and applying change control to production security changes.

## Repository layout

```text
Windows-Security-Incident-Investigation/
├── README.md
├── docs/
│   └── REPORT-REDACTION-NOTE.md
└── evidence/
    └── screenshots/
        └── README.md
```

## Evidence and report handling

The source report was supplied for preparing this portfolio case study. It is marked confidential/internal and includes endpoint-related details. Do not commit it in its original form to a public repository. Replace it only with a version approved for portfolio publication and sanitized of confidential information.

Screenshots and artifacts should be reviewed before addition. Remove or mask hostnames, usernames, account identifiers, contact information, internal paths, tokens, and other client-sensitive details.

## Disclaimer

This repository is a portfolio case study of investigation activities and evidence available within the stated scope. It is not a claim that the endpoint was fully cleared, that the exact malware execution path was established, or that monitoring was deployed across Cybugs production infrastructure.
