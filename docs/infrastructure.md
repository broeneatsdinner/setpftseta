# Infrastructure Overview

This document outlines the abstracted infrastructure used in SEPftSETA, designed to support passive adversary engagement while maintaining operational security and anonymity.

---

## Infrastructure Goals

- Preserve anonymity during inbound scammer interactions
- Route all communications through obfuscated network layers
- Collect metadata and traffic safely, with no exposure of personal systems
- Maintain ethical, transparent logging boundaries
- Use custom-built VPN and jump server infrastructure to avoid exposure through shared or pre-configured environments
- Maintain full control over network stack, logging, and SSH configuration to minimize third-party risk

---

## High-Level Architecture

```
[ Burner Device (Wi-Fi Only) ]
           │
           ▼
[ VPN Gateway - US-based VPS ]
           │
           ▼
[ Jump Server - EU-based VPS ]
           │
           ▼
[ Internet (VoIP, SMS, Web Links) ]
```

---

## Components

### 🔐 Burner Device
- A factory-reset iPhone 5
- Wi-Fi only — no SIM, no Apple ID
- Connects exclusively over VPN

### 🌐 VPN Gateway (Midwest, US)
- WireGuard-based VPN server hosted on a US-based VPS
- SSH hardened: `PermitRootLogin no`, key-based auth only
- Hand-rolled VPS with hardened SSH configuration (no root login, no password auth)
- No templates or pre-configured VPN appliances used — all setup and key generation performed manually
- Traffic encrypted and routed to jump server

### 🛫 Jump Server (Europe)
- Second VPS acting as the external-facing exit node
- Located in a privacy-conscious jurisdiction
- Hand-rolled and hardened, mirroring VPN gateway practices
- Traffic exits to VoIP provider and scammer-hosted infrastructure

### ☁️ VoIP Platform
- Anonymous number obtained via masked identity
- VoIP app installed on burner device
- Used to receive SMS/calls from threat actors

---

## Security Practices

- Public key authentication only — no password logins permitted
- No personally identifying usernames, hostnames, or comments in configuration
- Logs are collected on isolated systems with redacted metadata
- All IP addresses and providers abstracted in documentation and code

---

## Optional Future Enhancements

- DNS and HTTPS logging on jump server via `tcpdump` or `mitmproxy`
- Cowrie or Dionaea honeypot deployment behind jump server
- Reverse shell endpoint infrastructure (for future adversary interaction research)

---

## Disclaimer

All infrastructure was created for academic purposes and remains within the bounds of ethical passive collection. No offensive or unauthorized activities are conducted through this system.
