# 🛡️ Credential Stuffing Attack Simulation – Personal SOC Lab

**Lab Type:** Credential Stuffing Attack  
**Environment:** VMware | Kali Linux | Windows 11 | Splunk Enterprise | Ubuntu Server

## Objective

To simulate a **credential stuffing attack** from Kali Linux against a Windows 11 machine and detect the attack in **Splunk Enterprise** via log analysis, using real-time event forwarding and custom SPL queries.

## Lab Setup

| Component       | Details                                                    |
| --------------- | ---------------------------------------------------------- |
| **Attacker VM** | Kali Linux (Tools: Hydra, Burp Suite)                      |
| **Target VM**   | Windows 11 (RDP and local login attempts enabled)          |
| **SIEM**        | Splunk Enterprise on Ubuntu Server                         |
| **Log Source**  | Windows Event Logs + Sysmon via Splunk Universal Forwarder |

## Tools Used

- `hydra` – to automate the credential stuffing attack via RDP or SMB
- `eventvwr.msc` & Sysmon – to monitor and generate Windows security events
- Splunk Search Processing Language (SPL) – to detect and alert on brute-force patterns

## Attack Steps (Credential Stuffing)

1. Created a sample password list (`common_passwords.txt`)
2. Used `hydra` to attempt RDP login against Windows 11:
   ```bash
   hydra -t 4 -l admin -P common_passwords.txt rdp://<target_ip>
   ```

## Detection in Splunk

Windows Event Logs and Sysmon logs were forwarded to Splunk via the Universal Forwarder. The following SPL query was used to identify repeated failed login attempts:

```spl
index=wineventlog EventCode=4625
| stats count by Account_Name, Workstation_Name, _time
| where count > 5
```

This search aggregated failed login attempts (EventCode 4625) and identified usernames and machines with more than 5 failures, flagging credential stuffing behavior.

## Outcome

- Simulated credential stuffing attacks using Kali Linux and hydra
- Successfully detected brute-force login patterns using custom SPL in Splunk
- Demonstrated ability to integrate Windows logging and SIEM analysis in a lab environment
- Verified Windows event artifacts aligned with common brute-force techniques

## Key Learnings

- Credential stuffing generates identifiable event patterns (e.g., repeated EventCode 4625) that can be detected with proper log ingestion
- Sysmon enhances visibility into system behavior beyond standard event logs
- Splunk SPL is a powerful tool for real-time detection, aggregation, and correlation of attacker activity
- A functioning SIEM requires well-configured forwarding agents, log sources, and detection rules to be effective
