# 🦉 OBloodMap

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, the Go toolchain version it was built with, and every bundled
  component with its exact version and license. Feed it to Grype, Trivy or
  Dependency-Track to audit our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
