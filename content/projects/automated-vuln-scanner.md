---
title: "Automated Vulnerability Scanner & Threat-Intel Integrator"
date: 2025-09-10
weight: 3
summary: "A Python tool that automates Nmap-based scanning and enriches every finding with live threat intelligence from external REST APIs."
tags: ["Python", "Automation", "Threat Intel", "Nmap"]
ShowToc: true
---

> **TL;DR** — Turns raw scan output into context-aware, prioritized findings by combining automated scanning with external threat-intelligence enrichment.

🔗 **Repo:** [github.com/SahibGill386](https://github.com/SahibGill386)

## The problem

A flat list of open ports and service versions isn't actionable. What's *actually* exploited in the wild right now? Which finding deserves attention first? That context usually lives in external threat-intel sources — so I automated pulling it in.

## How it works

- **Discovery & scanning** driven through the **Nmap API** in Python
- **Enrichment** by querying external **threat-intelligence REST APIs** for each detected service / CVE
- **Prioritization** so output is ordered by real-world risk instead of scan order

## Stack

`Python` · `Nmap (python API)` · `RESTful threat-intel APIs` · automated reporting

## What it demonstrates

Security automation, API integration, and the instinct to enrich raw data with context — exactly the kind of tooling that makes a SOC or vuln-management team faster.
