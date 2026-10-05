## Remote Terminal Basics

### Terminal/TTY Background
- **Terminal server** = lets a host accept connections to its **command shell** or **GUI desktop** remotely
- Term "terminal" comes from old **TTY (teletype)** devices
- **TTY** = handles text input/output between user and the shell
- **Shell** = does the actual processing (the command environment)

### Terminal Emulators
- **Terminal emulator** = software that replicates TTY input/output function
- **Remote terminal emulator** = lets you connect to a **shell on a different host** over the network

---

## SSH (Secure Shell)

### Basics
- Main way to get **secure remote access** to:
  - UNIX/Linux servers
  - Network appliances (switches, routers, firewalls)
- Provides **encrypted** terminal emulation
- Also used for **SFTP** and other configurations

### Details
| Detail | Value |
|--------|-------|
| Default port | **TCP/22** |
| Most widely used implementation | **OpenSSH** |
| Available on | UNIX, Linux, Windows, macOS |

---

## Telnet

### Basics
- Both a **protocol** and a **terminal emulation tool**
- Transmits shell commands/output between client and remote host
- Default port: **TCP/23**

### Security Warning
- Can be password protected, BUT:
  - **Passwords and all communication = unencrypted**
  - Vulnerable to **packet sniffing** and **replay attacks**
- Historically used for switch/router configuration
- **Should NOT be used anymore** - use **SSH** instead for secure access

---

## RDP (Remote Desktop Protocol)

### Why RDP?
- SSH/Telnet = good for **command-line** only
- For **graphical desktop** access, you need a **GUI remote tool**
- GUI tools send: **screen + audio** data (host -> client) and **mouse/keyboard** input (client -> host)

### RDP Basics
- **RDP** = Microsoft's protocol for remote GUI access to **Windows** machines
- Default port: **TCP/3389**
- Admin can:
  - Set **permissions** for who can connect via RDP
  - Configure **encryption** on the connection

### Cross-Platform Support
- RDP **clients** available for: Linux, macOS, iOS, Android
  - (You don't need Windows to *connect to* an RDP server)
- Open-source RDP **servers** exist too, e.g., **xrdp**

---

## Quick Comparison Table

| Protocol | Port | Interface | Encrypted? | Common Use |
|----------|------|-----------|-------------|-------------|
| **SSH** | TCP/22 | Command-line | Yes | Secure remote shell access (Linux/network gear) |
| **Telnet** | TCP/23 | Command-line | No | Legacy, insecure - avoid using |
| **RDP** | TCP/3389 | Graphical (GUI) | Yes (configurable) | Remote Windows desktop access |

---

## Quick Summary
- **SSH** = secure command-line remote access (port 22) - replaces Telnet
- **Telnet** = old, insecure command-line remote access (port 23) - avoid
- **RDP** = Microsoft's GUI remote desktop protocol (port 3389)
- RDP clients exist on non-Windows platforms; xrdp = open-source RDP server
