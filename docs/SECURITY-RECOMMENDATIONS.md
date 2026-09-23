# Security Recommendations

## 1. Endpoint Protection

- Enable and maintain Windows Firewall.
- Enable Microsoft Defender Antivirus or the organization's
  approved endpoint protection solution.
- Review endpoint protection settings and ensure security
  controls cannot be disabled without authorization.
- Investigate and document any approved exceptions.

## 2. Logging and Centralized Monitoring

- Deploy Sysmon on relevant Windows endpoints to improve
  process and system activity visibility.
- Configure Splunk Universal Forwarder to send endpoint
  logs to the centralized monitoring platform.
- Monitor Windows Security, System, and relevant application
  logs.
- Verify that log forwarding remains operational.

## 3. Detection and Alerting

- Develop detections for suspicious process execution.
- Monitor unusual PowerShell and command-line activity
  where the required telemetry is available.
- Review repeated failed logons and other relevant
  authentication events.
- Establish alert handling and escalation procedures.

## 4. Security Awareness

- Educate employees about suspicious attachments and
  unexpected files received through messaging applications.
- Remind users to verify the sender before opening files.
- Provide a clear process for reporting suspicious messages
  and potential security incidents.

## 5. Incident Response

- Establish procedures for reporting, investigating,
  containing, and recovering from endpoint incidents.
- Preserve relevant logs and other evidence during
  investigations.
- Document incident timelines, findings, and evidence
  limitations.
- Coordinate with relevant technical teams when further
  endpoint or server-side investigation is required.

## 6. Change Control

- Document changes to endpoint security settings.
- Require appropriate authorization for disabling
  security controls.
- Periodically review security configurations and approved
  exceptions.

## 7. Implementation Status

This document records recommendations arising from the
investigation. It does not claim that the recommendations
have been implemented or independently verified.

## Related Documentation

- [Incident Timeline](INCIDENT-TIMELINE.md)
- [Investigation Searches](INVESTIGATION-SEARCHES.md)
- [Findings and Limitations](FINDINGS-AND-LIMITATIONS.md)
- [Security Incident Investigation Report](SECURITY_INCIDENT_INVESTIGATION_REPORT.pdf)
