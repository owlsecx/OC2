# 🦉 OC2

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OC2** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OC2 is an offline blue-team tool for finding signs of command-and-control (C2) frameworks. It scans files, directories, scripts and malleable C2 profiles for known C2 markers, extracts IOCs and decodes obfuscated blobs. It also generates Sigma detection rules. It only reads data and never connects to or controls anything.

---

## ✨ Features

- C2-marker scanner for files and directories covering Cobalt Strike, Sliver, Mythic, Metasploit, Havoc and others
- IOC extraction (IPs, URLs, emails, paths) with MITRE ATT&CK mapping
- Blob decoder: Shannon entropy grading plus base64, base64-UTF16, hex, ROT13 and single-byte XOR recovery
- Malleable C2 profile and config auditor
- Searchable catalog of 45 C2 techniques, Sigma-rule generator and ATT&CK coverage summary
- Reports in TXT / JSON / Markdown / CSV / SARIF; exits with code 3 on CRITICAL/HIGH findings

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OC2                                        # interactive menu
./OC2 --scan /path/to/suspicious_dir
./OC2 --profile malleable.profile
./OC2 --decode "<base64 blob>"
./OC2 --sigma > c2_rules.yml
```

Run `./OC2 --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
