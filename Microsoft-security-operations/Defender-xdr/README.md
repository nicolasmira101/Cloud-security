# Microsoft Defender XDR

- Extended Detection and Response (XDR)
- Microsoft Defender XDR is an integrated threat protection suite with solutions that detect malicious activity

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

- You can use [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) to run the hunting query

<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/graph-explorer-hunting-kql-query-2023-06-08.png"/>
</p>
