
## Mailbox Access Protocols (Overview)
- SMTP only delivers mail to **always-available server hosts**
- Received mail gets handed to a **mailbox server**
  - Could be a separate machine, or just a separate process on the same machine
- A **mailbox access protocol** lets the user's email client **retrieve** messages
- Two main protocols: **POP3** and **IMAP**

---

## POP3 (Post Office Protocol version 3)

### Basics
- Early mailbox access protocol
- "POP3" = version 3, the active version
- Client apps: Outlook, Thunderbird, etc.

### Ports
| Port | Security |
|------|----------|
| TCP/110 | Unencrypted |
| TCP/995 | Secure |

### How It Works
- User authenticates (username + password)
- Mailbox contents are **downloaded to the local PC**
- **Default behavior:** messages are **deleted from the server** after download
  - Some clients allow the option to **leave a copy on the server**

---

## IMAP (Internet Message Access Protocol)

### Basics
- Addresses POP's limitations
- Also a mail **retrieval** protocol, but with much better **mailbox management**

### Key Features
- Supports **permanent connections** to the server
- Multiple clients can connect to the **same mailbox simultaneously**
- Lets client **manage the mailbox on the server**:
  - Organize into **folders**
  - Control **when messages are deleted**
  - Create **multiple mailboxes**

### Ports
| Port | Security |
|------|----------|
| TCP/143 | Insecure |
| TCP/993 | Secure (IMAPS, uses TLS) |

---

## Quick Comparison: POP3 vs IMAP

| Feature | POP3 | IMAP |
|---------|------|------|
| Messages stored | Downloaded locally, usually **deleted from server** | Stay **on the server**, synced across devices |
| Multiple device access | Poor (mail "moves" to one device) | Good (mailbox stays in sync everywhere) |
| Server-side folder management | No | Yes |
| Standard port | 110 (995 secure) | 143 (993 secure) |
| Best for | Single device use | Multiple devices / webmail-style access |

---

## Quick Summary
- **POP3** = downloads mail to one device, usually removes it from server (ports 110/995)
- **IMAP** = keeps mail on server, syncs across multiple devices, supports folders (ports 143/993)
- IMAP is generally the **more modern/flexible** choice; POP3 is simpler but less convenient for multi-device use

