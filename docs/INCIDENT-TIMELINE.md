# Incident Timeline

## Overview

This timeline summarizes the incident sequence described in the
Security Incident Investigation Report.

The timeline distinguishes reported events from the SOC's subsequent
investigation activities. It does not assume that the exact malware
execution time or attack mechanism was confirmed.

## Timeline

| Date | Event |
|---|---|
| 9 September 2026 | A ZIP file received through WhatsApp from an unknown third party appeared to contain a video. The file was interacted with on three computers. |
| 9 September 2026 | Two computers were unable to play the file. The primary Windows endpoint was the computer on which the file was opened or interacted with. |
| 11 September 2026 | The same ZIP file was reportedly forwarded from the company's WhatsApp session without the user's intention. |
| During the investigation | The SOC collected Windows Event Log evidence and analyzed available Event ID 4688 process-creation records in Splunk Enterprise. |
| During the investigation | The SOC reviewed available process activity and conducted searches for selected suspicious utilities and user-writable paths. |
| During the investigation | The SOC documented findings, evidence limitations, and security recommendations in the investigation report. |

## Important Investigation Notes

- The VAPT/Bug-Bounty team classified the artifact as a Trojan.
  The SOC did not independently identify the malware family.
- The available Event ID 4688 records did not establish a confirmed
  execution chain linking the ZIP file to the WhatsApp forwarding.
- Sysmon and Splunk Universal Forwarder were not installed on the
  affected endpoint at the time of the incident.
- The absence of suspicious process names in the reviewed records
  does not prove that the endpoint was uncompromised.

## Scope and Limitations

This timeline is based on the incident information and investigation
findings documented in the report. It should not be interpreted as
a complete forensic reconstruction of the attack.

For the detailed methodology, evidence review, findings, and
recommendations, refer to:

`SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf`
