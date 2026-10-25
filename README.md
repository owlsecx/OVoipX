# 🦉 OVoipX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OVoipX** — VoIP / RTC Server Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OVoipX is an offline, read-only VoIP server configuration auditor for Asterisk and FreeSWITCH that parses sip.conf/pjsip.conf, extensions and FreeSWITCH XML with stdlib-only parsers. It flags default/weak SIP credentials, guest/anonymous access, toll-fraud dial-plan patterns, missing transport encryption (TLS/SRTP) and exposed management interfaces. Secrets are masked, findings are mapped to CWE and MITRE ATT&CK, and reports export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Parsers for Asterisk sip.conf/pjsip.conf/extensions.conf/manager.conf and FreeSWITCH XML/vars
- Credential checks: default/weak/plaintext SIP secrets (masked), guest/anonymous SIP access
- Toll-fraud dial-plan analysis (unrestricted outbound contexts, dangerous patterns)
- Transport security: missing TLS/SRTP, UDP SIP exposure and allowguest/allowtransfer risks
- Management-interface exposure (AMI/ARI, ESL) binding and credential review
- Secrets masked, CWE+ATT&CK mapping and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OVoipX --scan -f sarif -o voip.sarif
./OVoipX --sip /etc/asterisk/sip.conf --extensions /etc/asterisk/extensions.conf
./OVoipX -r /mnt/image --fail-on high --json
./OVoipX --demo
./OVoipX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
