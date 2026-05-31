---
title: "NetWatch — NIDS Simulator"
date: 2025-06-05
weight: 4
summary: "A Java desktop application that simulates a network intrusion-detection system: ingest logs, classify packets, flag suspicious activity."
tags: ["Java", "OOP", "IDS", "Software"]
ShowToc: true
---

> **TL;DR** — A from-scratch NIDS simulator in Java that ingests server logs, categorizes packet activity, and raises flags on suspicious behavior.

🔗 **Repo:** [github.com/SahibGill386](https://github.com/SahibGill386)

## Overview

NetWatch models how an intrusion-detection system processes traffic. It reads server logs, classifies packets, and flags activity that matches suspicious patterns — a way to internalize *how* detection logic works by building it.

## Design

Built on clean **object-oriented design**, keeping the pipeline decoupled:

- **Ingestion** — parse and normalize server log input
- **Classification** — categorize packets by type and characteristics
- **Alerting** — flag suspicious activity for review

## What it demonstrates

Solid software engineering (OOP, separation of concerns) applied directly to a security problem — the bridge between writing code and understanding detection internals.
