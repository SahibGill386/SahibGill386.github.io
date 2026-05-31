---
title: "Vulnerability Scanning Lab — Kali vs. Metasploitable 2"
date: 2025-04-20
weight: 2
summary: "A controlled vulnerability assessment that surfaced 335 CVEs and 18 confirmed-vulnerable findings — and the engineering report that prioritized them."
tags: ["Offensive Security", "Nmap", "Vulnerability Assessment", "Reporting"]
ShowToc: true
---

> **TL;DR** — Ran a full vulnerability assessment against an intentionally vulnerable target on an isolated network, pivoted tooling when the scanner broke, and wrote it up like a real engagement.

## Setup

A **VMware host-only network** isolating a Kali Linux attacker and a **Metasploitable 2** target — a deliberately vulnerable system used for safe, legal practice.

## When the plan broke

The original plan used **OpenVAS**, but it failed on a **PostgreSQL compatibility issue** that wouldn't resolve cleanly. Rather than stall, I pivoted to **Nmap NSE scripts** to drive the vulnerability discovery — a reminder that real assessments rarely go exactly as scripted.

## Findings

| Metric | Result |
| --- | --- |
| Scan passes | 2 |
| CVEs surfaced | **335** |
| Confirmed-vulnerable findings | **18** |

### Top prioritized vulnerabilities

- **`CVE-2011-2523` — vsftpd 2.3.4 backdoor.** A famous malicious backdoor that grants a root shell. Critical, trivially exploitable.
- **`CVE-2004-2687` — distccd remote code execution.** Arbitrary command execution via the distributed compiler daemon.
- **Apache Tomcat default credentials.** Default manager credentials left in place — a classic, high-impact misconfiguration.

## The part that matters

Anyone can run a scanner and dump 335 results. The skill is **triage**: separating noise from the handful of findings that actually let an attacker in, then communicating that clearly. The deliverable was a written report prioritizing remediation — the same artifact a real engagement produces.

*Completed as a collaborative course project; assessment, tooling pivot, and reporting documented above.*
