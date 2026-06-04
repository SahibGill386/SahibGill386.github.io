---
title: "Enterprise Active Directory Access Control & GPO Hardening"
date: 2026-05-15
weight: 4
summary: "Architected a secure Windows Server Active Directory environment enforcing Role-Based Access Control (RBAC) and system hardening via GPOs."
tags: ["Active Directory", "Windows Server", "GPO", "Access Control"]
ShowToc: true
---

> **TL;DR** — Deployed and audited a complete Windows Server Active Directory infrastructure implementing robust AGDLP identity design.

🔗 **Repo:** [://github.com](https://://github.com)

## The Problem
Default enterprise system configurations lack proper privilege controls, making them highly susceptible to horizontal credential theft or privilege escalation attacks.

## Hardening Actions Executed
- Enforced strict Password Complexity Policies and Account Lockout thresholds.
- Disabled legacy LLMNR and NetBIOS protocols via GPO to mitigate network poisoning threats.
- Configured restricted administrative groups utilizing Least Privilege principles.
