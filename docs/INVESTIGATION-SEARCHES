# Splunk Investigation Searches

This document summarizes the search activities and results recorded during the Windows security incident investigation at **Cybugs**.

## 1. Dataset Overview

| Attribute | Value |
|---|---|
| SIEM | Splunk Enterprise |
| Log Source | Windows Security Event Log |
| Event ID | 4688 |
| Event Type | Process Creation |
| Events Analyzed | 429 |
| Sourcetype | WinEventLog:Security |

## 2. Process Activity Review

### Objective
Review available process-creation events and examine process names and parent-child relationships.

### Investigation Dates
- 09 September 2026
- 11 September 2026

### Reported Results
The reviewed records primarily showed standard Windows system processes and expected parent-child relationships.

No suspicious process name was identified in the reviewed records for either date.

## 3. LOLBin Hunting

### Objective
Search the available Event ID 4688 dataset for selected commonly abused Windows utilities (LOLBins).

### Reported Result
No matching events were returned by the searches documented in the investigation report.

## 4. User-Writable Path Hunting

### Objective
Search for process execution from selected user-writable locations, including:

- Downloads
- AppData
- Temp
- Desktop

### Reported Result
No matching process-creation events were returned by the searches documented in the report.

## 5. Process Command-Line Availability

### Objective
Determine whether process command-line information was available in the imported dataset.

### Reported Result
No populated `Process_Command_Line` values were present in the imported dataset.

This limited the investigation's visibility into specific process parameters.

## 6. Interpretation and Limitations

The reported search results apply only to the available Event ID 4688 dataset and the searches performed.

The absence of matching events does not prove that malicious activity did not occur.

Sysmon and Splunk Universal Forwarder were not installed on the affected endpoint at the time of the incident. The available evidence therefore did not conclusively establish whether the suspicious artifact executed or establish a direct causal link between a specific process and the WhatsApp forwarding behavior.

## 7. SPL Query Availability

The investigation report describes the search objectives and results but does not reproduce the complete SPL expressions.

Exact SPL commands should be added only after they have been recovered from the original Splunk searches or independently rerun and validated against an appropriate dataset.

Do not present newly written queries as commands that were executed during the original investigation unless that is verified.
