----
# General basics

- Alert = Suspicious event (Malware detected on a device, clicked on phishing link, ..)
- Incident = group of related alerts believed to be of the same attack. Example attack:

1. Phishing email received → Alert
2. Malicious attachment opened → Alert
3. Malware installed → Alert
4. Credential theft detected → Alert
----
| Severity          | Color     | Meaning                                                                  |
| ----------------- | --------- | ------------------------------------------------------------------------ |
| **High**          | 🔴 Red    | Serious attack, likely human-operated, immediate investigation required  |
| **Medium**        | 🟠 Orange | Suspicious activity that could be part of an attack, needs investigation |
| **Low**           | 🟡 Yellow | Known/common malware or less severe suspicious activity                  |
| **Informational** | ⚪ Grey    | Security-related information, little or no immediate threat              |

**High**
- Ransomware
- Credential theft
- Security sensor tampering
- APT activity

**Medium**
- Suspicious file execution
- Anomalous registry changes
- Post-breach behaviors

**Low**
- Hack tools
- Reconnaissance commands
- Log clearing
- Common malware

**Informational**
- Potential security observations
- Awareness-related events
----
# Action center

The Action Center is the central place in Microsoft Defender XDR where you manage and monitor response and remediation actions.

Main functions:
- View remediation actions
- Approve or reject actions
- Track action status
- Review investigation history
- Undo supported actions
----
## Automated Investigation and Response (AIR)

AIR can:

- Investigate alerts automatically
- Determine if something is malicious
- Recommend remediation actions
- Execute or wait for approval (depending on automation level)

| Automation Level        | Approval Required?          |
| ----------------------- | --------------------------- |
| Full                    | No                          |
| Semi (Any Remediation)  | All actions                 |
| Semi (Core Folders)     | Only core/system folders    |
| Semi (Non-Temp Folders) | Only non-temp folders       |
| No Automation           | No automated actions at all |


All these actions appear in the Action Center.

**Common Response Actions**
- Isolate device
- Quarantine file
- Stop process
- Run antivirus scan
- Collect investigation package
- Block indicators (IOC)

**Automation Levels**
- Full Automation
**Defender investigates and remediates automatically.**
- Semi-Automation
**Defender investigates.
Analyst approves remediation actions.**

- Manual
**Defender provides findings only.
Analyst performs remediation.**

----
**Examen**

- Action Center = Remediation Management Dashboard
- Used for both manual and automated actions
- Closely tied to AIR (Automated Investigation and Response)
- Analysts can approve, reject, monitor, and undo actions
- Actions can come from:
  - Defender for Endpoint
  - Defender for Office 365
    Defender for Identity
Defender for Cloud Apps
----


## Microsoft Secure Score
Microsoft Secure Score is a measurement of your organization's security posture.

- A score showing your current security posture
- Improvement actions to increase security
- Recommendations prioritized by security impact

Common actions: 
- Enable MFA
- Configure Conditional Access
- Enable Microsoft Defender features
- Protect privileged accounts
- Reduce attack surface
- Enable device protection
----
## Reports

| Report                   | Purpose                  |
| ------------------------ | ------------------------ |
| Secure Score             | Security posture         |
| Threat Protection        | Attack and alert trends  |
| Vulnerability Management | Weaknesses and patches   |
| Device Health            | Device protection status |
| Email & Collaboration    | Phishing, spam, malware  |

----

## Email alerts

Email notifications are mainly used to notify about: 
- Alerts (e.g. Malware detected)
- Incidents
- Vulnerabilities
- Service/health issues (e.g. sensor health problems, device reporting issues)

----

# Microsoft Defender for Office 365

Most important features: 

## Safe attachments

- Checks email attachments in a secure sandbox before delivery.

Purpose: Block malware hidden in attachments.

## Safe links

- Scans URLs and checks them when users click them.

Purpose: Protect against malicious websites and phishing links.

## Anti-Phishing Protection

Detects: 

- Phishing emails
- Spoofing attacks
- Impersonation attacks
  
Purpose: Prevent credential theft.

## Anti-Malware Protection

- Scans emails and attachments for malware.

Purpose: Prevent malware delivery through email.
