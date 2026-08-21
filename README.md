# Footprinting & Network Scanning — Week 2 Pentesting Report

**Program:** Cybersecurity & Ethical Hacking Internship, Networkwalks (Batch B082)
**Modules:** W2-PM2 (Exploit Database) · W2-PM3 (Maltego) · W2-PM5 (Zenmap Scanning)
**Author:** Saran S — [LinkedIn](https://www.linkedin.com/in/saran-s21)
**Date:** 17 August 2026

---

## Overview

This repository contains my Week 2 practical report covering the **Reconnaissance & Footprinting** and **Scanning & Network Discovery** phases of a penetration test. It documents how an attacker (or a defender testing their own systems) moves from gathering public information about a target to mapping live hosts on a network and identifying possible vulnerabilities.

All activities were performed on:
1. `networkwalks.com` — with secured written permission
2. My own local LAN network

No exploitation was performed. This project is strictly an information-gathering and documentation exercise.

## Tools used

| Tool | Purpose |
|---|---|
| Kali Linux & Windows | Operating systems used for reconnaissance activities |
| Maltego | OSINT and link-analysis tool used to gather and visually connect information about a target |
| Zenmap (Nmap GUI) | Scans the local subnet to find live hosts, open ports, and services |
| Exploit Database | Searches for known, publicly disclosed vulnerabilities linked to specific software/services |
| Windows CMD | Local IP and MAC address identification |

## What's in this report

- **Footprinting & Reconnaissance (Maltego)** — ran OSINT transforms on the target domain to map linked entities, IP addresses, and infrastructure into a visual graph.
- **Network Scanning (Zenmap)** — identified live hosts on my local subnet, discovered open ports and running services, and generated a network topology.
- **Vulnerability Research (Exploit Database)** — cross-referenced the services/versions found during scanning against known, publicly disclosed vulnerabilities.
- **Risk analysis & recommendations** — practical, prioritized steps to reduce exposure based on the findings.
- **Evidence** — screenshots for every step, included in the full PDF report.

## Key findings (summary)

- Local scan identified live hosts, including a target machine exposing SMB (445), NetBIOS/RPC (135, 139), and multiple `msrpc` endpoints (49664–49680).
- Port 137 (NetBIOS) returned a filtered state, suggesting a firewall rule specific to that service.
- Maltego OSINT transforms surfaced publicly connected infrastructure and entity data tied to the target domain.
- Exploit Database searches linked discovered service versions to known, documented vulnerabilities — for awareness only, no exploitation attempted.

> Findings represent observations from information-gathering activities, not confirmed vulnerabilities. Further authorized testing would be required to validate any actual risk.

## Recommendations (summary)

1. Limit publicly available organizational information
2. Keep software and services patched and updated
3. Perform regular internal network scans
4. Close unused ports and services
5. Investigate unknown/unauthorized devices
6. Maintain up-to-date network documentation
7. Restrict access to sensitive services (SMB, RPC, NetBIOS)
8. Only test with proper authorization

## Repository contents

```
├── Maltego/                          # Screenshots and install/setup guide for Maltego
├── Nmap/                             # Screenshots and install/setup guide for Nmap
├── Exploit-DB/                       # Screenshots and usage notes for Exploit Database
├── README.md                         # This file
└── W2-PM-FINAL - Sample Report v2.pdf # Full PDF report with methodology and evidence
```

Each tool folder (`Maltego/`, `Nmap/`, `Exploit-DB/`) contains the screenshots captured during that activity, along with a short PDF walking through how the tool was downloaded and set up.

## Liability disclaimer

I performed these activities only on systems and devices I own, or where I had clear written permission to test. This repository is for education and learning purposes only. Nothing here should be used to break the law.

The instructor, authors, and Networkwalks are not responsible for how this information is used. Every action taken is the responsibility of the person doing it. Misusing these skills can lead to criminal charges, heavy fines, job loss, and a permanent criminal record. In most countries, accessing a system without permission is illegal even if no damage is caused.

---

**Author:** Saran S · Cybersecurity Professional, Batch B082
**Program:** Networkwalks Cybersecurity Internship | Week 02
