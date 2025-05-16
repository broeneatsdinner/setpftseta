# SEPftSETA

**Stealth Engagement Platform for Tracking Social Engineering Threat Actors**  
_A red team–inspired adversary engagement project_

---

## Overview

SEPftSETA is a cybersecurity research project focused on the passive collection, analysis, and documentation of unsolicited scam and phishing interactions. Designed with operational security in mind, this platform leverages anonymized infrastructure, VPN chaining, and OSINT techniques to safely observe threat actor tactics without exposing personal identity or initiating offensive action.

---

## Objectives

- Deploy a hardened, anonymized burner phone environment 
- Route communications through a chained VPN + jump server infrastructure
- Capture and log SMS, call metadata, and scam links sent to bait endpoints
- Record and transcribe both live scam calls and voicemails using Whisper, enriching with OSINT  
- Transcribe incoming scam voicemails using Whisper and enrich them with OSINT
- Perform passive DNS and HTTPS traffic analysis via isolated nodes
- Map language and behavioral patterns to MITRE ATT&CK framework
- Maintain ethical boundaries with no active probing or engagement

---

## Status

✅ Project proposal submitted – awaiting formal approval  
🔒 Infrastructure built with layered opsec  
📊 Passive logging, transcription, and enrichment pipeline in development  
📱 Burner phone (iPhone SE) acquired and prepped  
🧠 Final report and findings in progress — estimated completion: June 2025

---

## Documentation

- 📄 [Project Proposal](docs/project_proposal.md)
- 📁 [Infrastructure Overview](docs/infrastructure.md)
- 🔍 Redacted Traffic Logs *(in progress)*

---

## Ethics & OpSec

All data is collected passively from unsolicited attacker interaction.  
Infrastructure details (IP addresses, server locations, providers) are intentionally abstracted to preserve operational integrity. This project complies with ethical research standards and does not perform unauthorized access or offensive operations.

---

## Author

Broen Westberg  
🔗 [linkedin.com/in/broen](https://linkedin.com/in/broen)  
📍 Based in Denver, CO – open to hybrid red/purple team opportunities

---

## License

MIT License
