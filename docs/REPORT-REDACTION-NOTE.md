# Report publication checklist

The source investigation report is marked **CONFIDENTIAL – INTERNAL USE**. Keep the original report out of any public repository unless Cybugs has explicitly approved its release.

Before adding a portfolio-safe report:

- [ ] Obtain authorization to publish a sanitized case study.
- [ ] Confirm the company name is consistently written as **Cybugs**.
- [ ] Remove endpoint hostnames and other machine identifiers.
- [ ] Remove employee names, WhatsApp contacts, account details, and personal information.
- [ ] Remove internal file paths, infrastructure details, and any credentials or secrets.
- [ ] Review every screenshot, table, appendix, and PDF metadata field.
- [ ] Confirm the published findings stay within the available Event ID 4688 evidence.
- [ ] Preserve the stated limitations: Sysmon and Splunk Universal Forwarder were not present on the affected endpoint at the time.
- [ ] Do not describe the endpoint as clean or claim a confirmed execution mechanism based only on the absence of matching events.
- [ ] Have the final sanitized version reviewed and approved before committing it.
