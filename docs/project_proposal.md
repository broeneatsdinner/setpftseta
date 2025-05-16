# Project Proposal

**Title:** Design and Deployment of a Stealth Engagement Platform  
**Subtitle:** Tracking Social Engineering Threat Actors via Passive Infrastructure  
**Student:** Broen Westberg  
**Program:** Post Graduate Cybersecurity  
**Institution:** University of Denver  
**Date:** May 15, 2025  

---

## Project Overview

This project develops a stealth engagement platform to passively collect and analyze real-world scam and phishing interactions. Using anonymity-preserving infrastructure, VoIP baiting, and OSINT tooling, it captures unsolicited adversary behavior and documents tactics, techniques, and procedures (TTPs) within the MITRE ATT&CK framework.

The platform is designed for operational security, ethical transparency, and the collection of real-world threat intelligence in a controlled, passive environment.

---

## Justification for Project Selection

While initially considering a project involving RFID reverse-engineering and cloning, the scope was limited to hardware-level credential manipulation. This alternative project engages real adversaries, introduces deeper opsec planning, and leverages both blue team and red team techniques in a live environment. It also allows for open-ended analysis and adaptation during the engagement process.

---

## Objectives

- Deploy a burner phone environment using an iPhone 5 connected to Wi-Fi only  
- Route all outbound traffic through a custom VPN chain (U.S. → Europe) for anonymity  
- Acquire and configure a VoIP number anonymously (e.g., via TextNow, MySudo, or JMP.chat)  
- Log incoming scam calls and SMS texts for analysis  
- Conduct safe OSINT on inbound phone numbers and URLs  
- Optionally respond to or re-engage scammers using scripted interaction over VoIP  
- Analyze captured behavior and map it to MITRE ATT&CK techniques and tactics  
- Present findings with ethical commentary and procedural documentation  

---

## Technical Framework

- **Burner Device**: Hardened iPhone 5 with no SIM or Apple ID  
- **Anonymity Layer**: Self-hosted VPN + international jump server on remote VPS  
- **VoIP Platform**: Secure VoIP app tied to masked identity  
- **Logging**: Timestamps, metadata, screenshots, SMS records  
- **Enrichment Pipeline**: Processes raw data (phone numbers, domains, IPs) into contextual threat intelligence using VirusTotal, WHOIS, AbuseIPDB, and passive DNS  
- **OSINT Tools**: VirusTotal, WHOIS, AbuseIPDB, reverse phone lookup  
- **Network Analysis**: Nmap, mitmproxy, Wireshark (in sandboxed VM)  
- **Honeypot Option**: Cowrie for SSH probing, Dionaea for malware capture (if time allows)  
- **MITRE ATT&CK Mapping**: Document and categorize attacker behavior  

---

## Ethical Considerations

- No engagement will intentionally provoke malicious actors  
- No illegal access, credential reuse, or offensive actions will be taken  
- Only publicly available or unsolicited inbound content will be analyzed  
- The project emphasizes passive logging, transparency, and academic reporting  

---

## Expected Deliverables

- A functioning, anonymized scam monitoring platform  
- A collection of sanitized call logs, SMS messages, and metadata  
- OSINT enrichment results and TTP documentation  
- MITRE ATT&CK mapping of observed behaviors  
- Public GitHub repository documenting design, logs (redacted), and tooling  
- A final written report and live demonstration (if safe and applicable)  

---

## Future Potential Enhancements

While this project is scoped for completion in a condensed two-week timeframe, future iterations could expand into more offensive security tooling. This includes the integration of:

- **Burp Suite** for analyzing phishing infrastructure and reverse-engineering scam payloads  
- **BeEF (Browser Exploitation Framework)** for hooking scammer browsers during controlled bait engagement  

These capabilities are discussed for future use only and will not be implemented in this project’s timeline. No active offensive tooling will be deployed in this engagement.

---

## Conclusion

This project offers a realistic, safe, and flexible approach to studying modern social engineering tactics in the wild. It leverages cybersecurity tooling across the stack, while reinforcing operational security, ethical awareness, and real-world threat intelligence methodology. It is well-suited for a master’s-level demonstration of red/blue team integration and investigative initiative.
