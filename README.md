# Microsoft Sentinel Detection Engineering Lab — RDP Honeypot & Threat Investigation

> Cloud SIEM lab demonstrating Windows RDP honeypot telemetry, failed-login analysis, PowerShell-based event enrichment, geographic visualization, and threat investigation using Microsoft Sentinel.

## Security workflow

```text
Internet-facing honeypot
        ↓
Windows Security Events
        ↓
PowerShell collection / enrichment
        ↓
External IP geolocation
        ↓
Microsoft Sentinel
        ↓
Detection & Investigation
        ↓
Geographic visualization
```

## Objective

The original lab captured failed RDP authentication attempts against a controlled Windows honeypot hosted in Microsoft Azure.

The project demonstrates how raw Windows security events can be collected, enriched with external IP context, ingested into a cloud SIEM, and visualized for investigation.

## Architecture

| Component | Role |
|---|---|
| Windows 10 Pro | Controlled honeypot |
| Microsoft Azure | Cloud hosting |
| Windows Event Logs | Authentication telemetry |
| PowerShell | Event extraction/enrichment |
| IP geolocation API | Source-context enrichment |
| Microsoft Sentinel | SIEM, analytics and visualization |

## Detection scenario

The honeypot received repeated failed RDP authentication attempts.

The investigation workflow was:

```text
Failed RDP login
      ↓
Windows Event Log
      ↓
PowerShell extraction
      ↓
Source IP enrichment
      ↓
Microsoft Sentinel
      ↓
Geographic visualization
      ↓
Threat investigation
```

The historical lab captured repeated activity from multiple geographic locations over several days.

## What this demonstrates

- Cloud-hosted security monitoring
- Windows authentication telemetry
- RDP attack-surface monitoring
- PowerShell security automation
- External threat-intelligence enrichment
- SIEM ingestion
- Geographic threat visualization
- Investigation-oriented security analytics

## Portfolio relevance

This project demonstrates the SIEM side of the security-engineering workflow:

**Telemetry → Enrichment → Detection → Investigation**

It complements the Wazuh project, which focuses more heavily on endpoint detection and FIM.

## Evidence

The original repository contains screenshots showing:

- Live failed-login activity
- Geographic source information
- Microsoft Sentinel world-map visualization
- Activity observed across multiple days

> Historical screenshots are retained as evidence of the original lab. The project should be interpreted as a lab demonstration, not as a current production Sentinel deployment.

## Modernization notes

The project originally used the name **Azure Sentinel**. Microsoft Sentinel is the current product name.

For a new implementation, the lab should be rebuilt using current Microsoft Sentinel workflows and the current Microsoft Defender portal experience.

## Recommended next iteration

- Rebuild ingestion using current Microsoft Sentinel data connectors
- Add KQL queries for failed RDP authentication
- Create an analytic rule for repeated failures
- Map the detection to MITRE ATT&CK
- Add entity mapping for source IP and account
- Create an incident investigation workflow
- Add false-positive tuning
- Document response recommendations
- Reproduce the visualization with current Sentinel capabilities

## Responsible use

The honeypot was designed for controlled security research. Never expose intentionally vulnerable systems to the public Internet without appropriate isolation, monitoring, authorization and risk controls.

## Author

**Toluwalase Owolabi**

Focus areas: Security Operations, Detection Engineering, SIEM, Cloud Security, Vulnerability Management and AI Security.
