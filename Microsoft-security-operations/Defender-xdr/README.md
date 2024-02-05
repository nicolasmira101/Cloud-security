# Microsoft Defender XDR

- Extended Detection and Response (XDR)
- Microsoft Defender XDR is an integrated threat protection suite with solutions that detect malicious activity.
- Natively coordinates detection, prevention, investigation, and response across endpoints, identities, email, and applications.

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/defend-attack-chains.png"/>
</p>

## XDR response use cases

- This scenario depicts a case where Microsoft Defender for Endpoint detects a malicious payload (which could come from any source, including personal email or a USB drive).

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/compromised-endpoint.png"/>
</p>

- Microsoft Defender for Endpoints (MDE) detects this attack, raises an alert to security operations
- The Conditional Access created in Microsoft Entra ID blocks user access to apps.
  
<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/suspend-access-compromise.png"/>
</p>

## Microsoft Defender XDR in a SOC

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/security-operations.png"/>
</p>

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/security-operations-model.png"/>
</p>

- Automation: near real-time resolution of known incident types with automation.
- Tier 1: analysts focus on rapid remediation of a high volume of well-known incident types that still require human judgment.
- Tier 2: this team provides deeper investigation into a lower volume of more complex attacks.
- Tier 3: proactively hunts for undetected threats, advanced forensics for reactive investigations, and refines alerts/automation.
- Threat Intelligence teams: provide context and insights to support all other functions.

## Microsoft Security Graph

- Provides a unified programmability model that you can use to access the data in Microsoft 365 and Windows.
- The Microsoft Graph API offers a single endpoint, https://graph.microsoft.com

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/graph-security-overview-diagram.png"/>
</p>

- Developers can use the Security Graph to build intelligent security services
- Advanced hunting example in Microsoft Defender XDR

```
POST https://graph.microsoft.com/v1.0/security/runHuntingQuery

{
    "Query": "DeviceProcessEvents | where InitiatingProcessFileName =~ \"powershell.exe\" | project Timestamp, FileName, InitiatingProcessFileName | order by Timestamp desc | limit 2"
}
```

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/graph-explorer-hunting-kql-query-2023-06-08.png"/>
</p>

## Microsoft Defender portal

- The [Microsoft Defender portal](https://security.microsoft.com/) is a specialized workspace designed to meet the needs of security teams.
- You can investigate the alerts that affect your network, understand what they mean, and collate evidence.
- The Microsoft Defender portal brings together signals from different sources to present a holistic view of Microsoft 365 environment.
- The Microsoft Defender portal combines protection, detection, investigation, and response, in a central place.

## Incidents Response

- Microsoft Defender XDR provides a cross-domain threat correlation and purpose-driven portal to investigate threats.
- Incidents are based on related alerts created when a malicious event or activity is seen on your network.
- An incident is a collection of correlated alerts that make up the story of an attack.
- Microsoft Defender XDR automatically aggregates malicious and suspicious events that are found in different device.
- Grouping related alerts into an incident gives security defenders a comprehensive view of an attack.
- Managing incidents is critical in ensuring that threats are contained and addressed.
- Microsoft Defender XDR is aligned to the MITRE ATT&CK™ framework.
- Investigate alerts that are affecting your network, understand what they mean, and how to resolve them.
- Microsoft Defender for Endpoint includes automated investigation and remediation (AIR) capabilities.

## Advanced hunting

- Is a query-based threat-hunting tool.
- You can proactively inspect events in your network to locate threat indicators and entities.
-  
