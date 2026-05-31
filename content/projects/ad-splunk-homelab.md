---
title: "Active Directory + Splunk SIEM Homelab"
date: 2025-11-15
weight: 1
summary: "A full enterprise-style detection environment — Active Directory, Splunk, and Snort — that I attack with Kali to prove the detections actually fire."
tags: ["Detection Engineering", "Splunk", "Active Directory", "Snort", "Blue Team"]
cover:
  alt: "AD + Splunk homelab"
ShowToc: true
---

> **TL;DR** — I built a complete Windows enterprise environment from scratch, wired it into a SIEM, then attacked it with Kali and Metasploit to validate that my detection rules trigger on real adversary behavior.

🔗 **Repo:** [github.com/SahibGill386/Active-Directory-Splunk-Homelab](https://github.com/SahibGill386/Active-Directory-Splunk-Homelab)

## Why I built it

Reading about detection isn't the same as watching an alert fire because *you* just ran the attack that triggered it. I wanted an environment where I could control both sides of the fight — stand up realistic infrastructure, attack it, and engineer the detections that catch the attack.

## What's in the lab

- **Active Directory** domain with Group Policy, organizational units, and managed user accounts
- **DNS / DHCP** services and **VLAN segmentation** to model a realistic network boundary
- **Splunk** as the SIEM, ingesting logs from **Windows Universal Forwarders**
- **Snort** as a network IDS watching east-west and north-south traffic
- All virtualized on **VMware**, fully isolated

## The attack → detect loop

1. **Attack** from a Kali box using Metasploit and standard offensive tooling against the domain.
2. **Observe** the telemetry land in Splunk (Windows event logs) and Snort (network alerts).
3. **Engineer** the detection — tune searches and rules so the malicious behavior surfaces cleanly without drowning in false positives.
4. **Re-run** to confirm the detection fires reliably.

## What it demonstrates

Enterprise infrastructure setup, SIEM pipeline design, log-source onboarding, IDS deployment, and — the part that matters most — the discipline of *validating* detections against live attacks instead of assuming they work.
