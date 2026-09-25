---
title: Simple CTF
date: 2026-03-15
platform: TryHackMe
category: Web
difficulty: easy
url: https://tryhackme.com/room/simplectf
lang: pt
tags: [web, sqli, linux]
summary: Primeiro contato com exploração web. Encontrei um diretório exposto e uma falha de upload.
---

# Simple CTF — TryHackMe

## Reconhecimento

Rodei `nmap -sV 10.10.123.45` e encontrei:

- Porta 21 (FTP)
- Porta 80 (HTTP)
- Porta 2222 (SSH)

## Enumeração

O site na porta 80 rodava **Apache**. Usei o Gobuster:

```bash
gobuster dir -u http://10.10.123.45 -w /usr/share/wordlists/dirb/common.txt
```

Achei o diretório `/simple/`.

## Exploração

O login era vulnerável a **SQL Injection**:

```sql
' OR 1=1--
```

## Flag

`flag{encontrei_a_flag_aqui}`

## O que aprendi

- Nmap com `-sV` mostra versões
- SQL Injection básico ainda funciona
- Sempre vale rodar Gobuster em sites Apache