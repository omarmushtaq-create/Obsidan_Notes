
## Email Basics
- Lets users send messages to someone on the **same network (intranet)** or **anywhere via the Internet**
- Uses **two types** of mail protocols:
  - **Mail transfer** protocols (moving mail between servers)
  - **Mailbox access** protocols (retrieving mail from a mailbox)

---

## Email Delivery Process (4 Steps)

| Step | What Happens                                                                                                                                                   |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Client submits message to **local SMTP server** (secure port **587**); message is also copied to **Sent Items** on local **IMAP server** (secure port **993**) |
| 2    | Local SMTP server looks up the recipient's domain **MX record** via DNS, then connects to the **remote SMTP server** over **unencrypted port 25**              |
| 3    | If accepted, remote server copies the message into the **Inbox** on the recipient's **IMAP server**                                                            |
| 4    | Recipient's mail client connects to their **IMAP server** over secure port **993** to download the message                                                     |
|      |                                                                                                                                                                |

> **Simple version:** You send mail out over 587 -> it hops server-to-server over 25 -> lands in the recipient's inbox -> they pull it down over 993.

---

## Email Address Format
- Follows the **mailto URL scheme**
- Format: `username@domain`
  - **Username (local part)** = before the @
  - **Domain name** = after the @ (company or ISP)

### Example
```

[david.martin@comptia.org](mailto:david.martin@comptia.org)

```

---

## SMTP (Simple Mail Transfer Protocol)

### Purpose
- Defines how email is **delivered between mail domains**
- Sender's SMTP server finds the recipient's SMTP server IP using **DNS**
  - Looks up **MX records** and the associated **A/AAAA host records**

### SMTP Ports

| Port | Used By | Purpose | Security |
|------|---------|---------|----------|
| **TCP/25** | Server-to-server (MTA to MTA) | Message **relay** between SMTP servers | Usually **unencrypted** |
| **TCP/587** | Mail client to server (MSA) | Client **submits** message for delivery | Should use **encryption + authentication** |

### Key Terms
| Term | Meaning |
|------|---------|
| **MTA** (Message Transfer Agent) | Server relaying mail to another server (port 25) |
| **MSA** (Message Submission Agent) | Handles client message submission (port 587) |

---

## Quick Summary
- Email delivery = **SMTP** (sending/relay) + **IMAP** (mailbox access/retrieval)
- Port **587** = client submits mail (secure)
- Port **25** = server-to-server relay (usually unencrypted)
- Port **993** = secure IMAP (retrieving mail)
- SMTP server finds the destination server using **DNS MX records**
- Email address = `username@domain` (mailto URL scheme)

