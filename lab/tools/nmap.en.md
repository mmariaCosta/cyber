---
title: Nmap
date: 2026-01-15
lang: en
status: ready
category: Network
role: Network mapping and port scanning
url: https://nmap.org
tags: [network, scan, recon]
---

# Nmap

Essential tool for **reconnaissance**.

## Commands I use

```bash
nmap -sn 192.168.1.0/24    # active hosts
nmap -sV 192.168.1.10      # ports + versions
nmap -p- -A 192.168.1.10   # full scan
```