# DFIR Investigation Case Files

**Author:** Himanshu Chourasia — Senior DFIR Engineer  
**LinkedIn:** [linkedin.com/in/chourasia04](https://www.linkedin.com/in/chourasia04/)  
**Experience:** 3+ years | Federal Law Enforcement (CBI) + Enterprise IR (Hitachi Systems)

---

## About This Repository

This repository contains senior-level Digital Forensics & Incident Response (DFIR) investigation writeups. Each case is a realistic scenario modelled on common enterprise and law enforcement threat patterns, documented to the standard of legally defensible forensic reporting.

All investigations include:
- Full attacker timeline reconstruction
- MITRE ATT&CK TTP mapping
- Tool commands with annotated output
- Indicators of Compromise (IOCs)
- Executive summary + technical findings
- Lessons learned and detection recommendations

---

## Case Index

| # | Case | Type | Key Tools | ATT&CK Tactics |
|---|------|------|-----------|----------------|
| [01](./01-ransomware-ir/) | **BlackCat Ransomware — Enterprise Outbreak** | Ransomware IR | KAPE, Hayabusa, CrowdStrike, EZTools | Initial Access, Lateral Movement, Impact |
| [02](./02-memory-forensics/) | **Fileless Malware via Process Injection** | Memory Forensics | Volatility 3, Malfind, PsList | Defense Evasion, Execution, Persistence |
| [03](./03-log-analysis/) | **BEC & Credential Harvesting — Splunk Investigation** | Log Analysis | Splunk SPL, Chainsaw, Sigma Rules | Initial Access, Credential Access, Exfiltration |
| [04](./04-mobile-forensics/) | **Insider Data Exfiltration via Android Device** | Mobile Forensics | Cellebrite UFED, MSAB XRY, Magnet AXIOM | Collection, Exfiltration, Insider Threat |
| [05](./05-malware-triage/) | **Cobalt Strike Beacon — C2 Triage & Attribution** | Malware Triage | Volatility, KAPE, CrowdStrike Falcon, PEStudio | Command & Control, Persistence, Discovery |
| [06](./06-network-forensics/) | **Covert C2 Over DNS Tunnelling** | Network Forensics | Wireshark, Zeek, CrowdStrike Falcon, tshark | C2, Exfiltration, Defense Evasion |
| [07](./07-threat-hunting/) | **Dormant APT — WMI Persistence Hunt** | Threat Hunting | CrowdStrike Falcon, Zeek, Hayabusa, KAPE | Persistence, Lateral Movement, Defense Evasion |

---

## Tooling Used Across Cases

| Category | Tools |
|----------|-------|
| **Acquisition & Triage** | KAPE, EZTools, CyberTriage |
| **Memory Forensics** | Volatility 3 (Windows & Linux) |
| **Disk & Artifact Analysis** | Magnet AXIOM, Autopsy, FTK |
| **Log Analysis** | Splunk SPL, Hayabusa, Chainsaw, Sigma |
| **EDR Telemetry** | CrowdStrike Falcon |
| **Mobile Forensics** | Cellebrite UFED 4PC, MSAB XRY, Magnet AXIOM |
| **Malware Analysis** | PEStudio, VirusTotal, Any.run, CAPA |

---

## Methodology

All investigations follow the **NIST SP 800-61r2** Incident Response lifecycle:

```
Preparation → Detection & Analysis → Containment → Eradication → Recovery → Post-Incident
```

Forensic integrity is maintained throughout via:
- SHA-256 hashing of all acquired evidence
- Write-blocker usage on physical media
- Documented chain of custody
- Tamper-evident evidence packaging

---

## MITRE ATT&CK Coverage

```
Initial Access        ████████████  TA0001
Execution             ████████████  TA0002
Persistence           ████████████  TA0003
Privilege Escalation  ████████      TA0004
Defense Evasion       ████████████  TA0005
Credential Access     ████████      TA0006
Discovery             ████████      TA0007
Lateral Movement      ████████      TA0008
Collection            ████████████  TA0009
Command & Control     ████████████  TA0011
Exfiltration          ████████████  TA0010
Impact                ████████████  TA0040
```

---

> **Disclaimer:** All scenarios, hostnames, IP addresses, usernames, and company names used in these writeups are created for educational and portfolio purposes only. No real case data, evidence, or sensitive information is disclosed.
