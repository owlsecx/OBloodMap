# 🦉 OBloodMap

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OBloodMap** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OBloodMap helps blue teams find and fix the riskiest attack paths in Active Directory. It loads a BloodHound JSON export or a simple edge CSV, builds a graph and ranks the shortest paths from low-privilege or owned accounts to high-value targets such as Domain Admins and domain controllers. It works fully offline and never touches a live domain.

---

## ✨ Features

- Parses BloodHound JSON ({nodes,edges} / {data}) and simple source,edge,target CSV files
- Ranks shortest attack paths from owned or low-privilege principals to high-value targets
- Dangerous-ACL findings (GenericAll, WriteDACL, DCSync, AddKeyCredentialLink and more) graded with ATT&CK mapping
- Graph statistics and an edge-abuse reference catalog
- Demo graph generator for training and testing
- Reports in TXT / JSON / Markdown / CSV / SARIF; exits with code 3 on CRITICAL/HIGH findings

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBloodMap                                  # interactive menu
./OBloodMap --analyze bloodhound.json
./OBloodMap --paths bloodhound.json
./OBloodMap --catalog
```

Run `./OBloodMap --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
