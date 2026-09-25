---
title: Nmap
status: ready
category: Rede
role: Mapeamento de rede e scan de portas
url: https://nmap.org
lang: pt
tags: [rede, scan, recon]
---

# Nmap

Ferramenta essencial pra **reconhecimento** — descobrir hosts ativos e portas abertas.

## Comandos que uso

\`\`\`bash
# Descobre hosts ativos na rede
nmap -sn 192.168.1.0/24

# Scan de portas + versões de serviço
nmap -sV 192.168.1.10

# Scan completo (mais lento)
nmap -p- -A 192.168.1.10
\`\`\`

## Aprendizado

Foi a **primeira ferramenta** que aprendi. Base pra qualquer pentest.