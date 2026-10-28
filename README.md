# SOC Investigation Lab — Network Traffic Analysis & Incident Response

## Overview

A hands-on Security Operations Center (SOC) investigation project focused on network traffic analysis, security alert validation, indicator of compromise (IOC) identification, and incident response recommendations.

Using packet captures from security training exercises, I investigate suspicious network activity, reconstruct event timelines, and map observed behaviors to the MITRE ATT&CK framework.

Each investigation includes supporting evidence, an assessment of findings and confidence, and actionable recommendations for containment, remediation, and detection improvement.

## Objectives

- Investigate suspicious network activity using Wireshark and packet captures.
- Validate security alerts against observable network evidence.
- Reconstruct incident timelines using packet timestamps and protocol analysis.
- Extract and document IOCs, including IP addresses, URLs, file names, and SHA-256 hashes.
- Map observed adversary behaviors to relevant MITRE ATT&CK techniques.
- Assess evidence limitations and distinguish confirmed findings from unverified activity.
- Develop incident response recommendations based on investigation results.

## Tools & Frameworks

- **Network Analysis:** Wireshark
- **Investigation Techniques:** Packet inspection, TCP stream analysis, HTTP analysis, DNS analysis, file extraction, SHA-256 hashing
- **Threat Intelligence:** IOC identification and documentation
- **Framework:** MITRE ATT&CK
- **Reporting:** Incident timelines, evidence-based findings, confidence assessments, and remediation recommendations

## Featured Investigation: NatureForce Exercise

**Scenario:** Investigation of suspicious executable delivery and a separate command-and-control (C2) alert in a simulated Windows environment.

**Investigation highlights:**
- Analyzed a packet capture to identify the affected Windows host and reconstruct relevant network activity.
- Confirmed an executable download over HTTP on TCP port 9000 using packet-level evidence.
- Reconstructed the download transaction and verified the transferred file size against the HTTP response and reassembled TCP stream.
- Calculated a SHA-256 hash for the extracted executable and documented associated IOCs.
- Evaluated a separate C2 alert and documented that the available capture did not contain supporting traffic.
- Mapped observed behavior to MITRE ATT&CK and developed prioritized incident response recommendations.

**Key takeaway:** The investigation distinguishes confirmed file delivery from unverified C2 activity and undetermined process execution, demonstrating an evidence-driven approach to incident analysis.

[Read the full NatureForce investigation report](investigations/natureforce/incident-report.md)

## Investigation Workflow

1. **Alert Triage:** Identify the security alerts and determine what evidence is needed.
2. **Traffic Analysis:** Inspect packet captures, protocols, endpoints, and relevant TCP streams.
3. **Timeline Reconstruction:** Correlate packet timestamps and build a chronological sequence of events.
4. **IOC Extraction:** Identify and document relevant network and file indicators.
5. **Alert Validation:** Determine whether available evidence supports, contradicts, or leaves an alert unresolved.
6. **MITRE ATT&CK Mapping:** Associate observed behaviors with applicable techniques when supported by evidence.
7. **Incident Reporting:** Document findings, confidence, limitations, and recommended response actions.


## Skills Demonstrated

- Network traffic analysis and packet inspection
- Security alert validation and triage
- HTTP, DNS, and TCP stream analysis
- Incident timeline reconstruction
- IOC extraction and documentation
- MITRE ATT&CK mapping
- Evidence-based incident reporting
- Incident containment and remediation planning

## Data Sources & Disclaimer

Investigations use publicly available cybersecurity training exercises and simulated network traffic. Findings are limited to the evidence available in each dataset and do not imply access to or investigation of a live production environment.

Malicious indicators are defanged in documentation where appropriate. Any extracted files should be handled in an isolated, authorized analysis environment.
