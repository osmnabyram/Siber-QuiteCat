<div align="center">

# QuiteCat

### A menu-driven helper for managing Metasploit reverse TCP listeners.

Keeps LHOST/LPORT configuration, `multi/handler` startup, and a set of post-exploitation cheat commands in one place, so you spend less time retyping handler setup on MSFConsole.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Metasploit](https://img.shields.io/badge/Requires-Metasploit-e53935?style=for-the-badge&logo=metasploit&logoColor=white)
![Purpose](https://img.shields.io/badge/Use-Authorized%20testing%20only-121212?style=for-the-badge)

</div>

<div align="center">
<img width="1908" alt="QuiteCat interface" src="https://github.com/user-attachments/assets/e6d20b66-d03c-4933-a1b4-b640b89aa5d9" />
</div>

---

## Overview

Setting up a reverse TCP listener on Metasploit means the same handler commands every time. QuiteCat wraps that in a small menu: it validates and stores LHOST/LPORT, launches `exploit/multi/handler` with the right payload, and keeps a reference sheet of common MSFConsole commands for the post-exploitation phase.

---

## Menu Options

| Option | Action |
|---|---|
| 1 — Cheat Codes | Frequently used MSFConsole commands and scenario-based examples |
| 2 — Update Settings | Set LHOST and LPORT with IP/port validation |
| 3 — Start Listener | Launch a reverse TCP listener via `exploit/multi/handler` |
| 0 — Exit | Clean exit |

---

## Listener Behaviour

- `msfconsole` launched in quiet mode (`-q`)
- Uses `exploit/multi/handler`
- Default payload `windows/meterpreter/reverse_tcp`
- LHOST and LPORT set automatically from your saved configuration
- Listener runs as a background job (`-j`)

---

## Features

- Menu-driven interface
- Validated LHOST / LPORT configuration management
- Automatic `multi/handler` initialization
- IP address and port validation
- Reference cheat-sheet for learning MSF post-exploitation commands
- ASCII banner and loading animation

---

## Requirements

| Component | Notes |
|---|---|
| Python 3.x | Interpreter |
| Metasploit Framework | Provides `msfconsole` |
| Linux + terminal access | Tested on Linux |

---

## Installation

```bash
git clone https://github.com/osmnabyram/Siber-QuiteCat.git
cd Siber-QuiteCat
chmod +x QuiteCat.py
python3 QuiteCat.py
```

Set your LHOST/LPORT from the menu before starting a listener.

---

## Responsible Use

QuiteCat is a convenience wrapper around Metasploit intended **only** for education and for engagements you are explicitly authorized to perform. Using it against systems without permission is illegal. The author accepts no liability for misuse.
