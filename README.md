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

Offline VoIP / RTC server configuration auditor (Asterisk, FreeSWITCH, Kamailio, XMPP)

---

## ✨ Features

- Offline, read-only auditing of VoIP/RTC configs — nothing is sent on the network, nothing is modified
- Asterisk chan_sip (sip.conf) + chan_pjsip (pjsip.conf) parser with templates, #include and inheritance
- Dialplan analyzer (extensions.conf) — include-graph reachability from untrusted contexts to outbound trunks (toll fraud), System()/Shell() injection, unfiltered ${EXTEN} patterns, DISA, remote AGI
- AMI (manager.conf), HTTP (http.conf) and ARI checks
- FreeSWITCH vars.xml / event_socket / sofia / acl / directory / xml_rpc analyzer
- Kamailio / OpenSIPS .cfg with #!define/#!ifdef preprocessor — pike, ratelimit, REGISTER auth, TLS
- Prosody (prosody.cfg.lua) and ejabberd (ejabberd.yml) analyzers with a built-in mini YAML / Lua parser
- Weak-secret engine (masked — secrets never printed)
- CWE + MITRE ATT&CK mapping, score & A+…F grade
- Exports TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Hardened configuration templates for every platform
- Self-test demo (weak vs hardened corpora)
- Full CLI mode (--asterisk, --root, --scan, ...)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OVoipX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
