
## The Problem with HTTP
- HTTP = **no encryption**, **no authentication** of client or server
- All data sent **in plaintext**
- Major security issue for early websites

---

## SSL and TLS

### History
| Protocol | Origin |
|----------|--------|
| **SSL** (Secure Sockets Layer) | Developed by **Netscape** in the 1990s |
| **TLS** (Transport Layer Security) | Developed from SSL, ratified as a standard by the **IETF** |

> TLS is the modern successor to SSL - "SSL" is still used colloquially, but TLS is the actual standard in use today.

---

## HTTPS
- **HTTP + TLS = HTTPS**
- Uses **TCP port 443** (encrypted) instead of port 80 (unencrypted)

### TLS Isn't Just for HTTP
TLS can secure other protocols too:
- FTP
- POP3/IMAP
- SMTP
- LDAP

> **Naming pattern:** If there's an "S" at the **end** of the acronym (HTTPS, SMTPS, LDAPS) = secured via SSL/TLS

### Note: DTLS
- TLS can also work over **UDP** -> called **DTLS** (Datagram TLS)
- Most often used in **VPN** solutions

---

## How HTTPS Works (Digital Certificates)

### Setup
- Web server installs a **digital certificate** issued by a trusted **Certificate Authority (CA)**
- Certificate proves the server's **identity** to the client (assuming client trusts the CA)

### Public/Private Key Pair
| Key | Who Has It | Purpose |
|-----|------------|---------|
| **Private key** | Server only (secret) | Used to decrypt / prove identity |
| **Public key** | Given to clients via certificate | Used to encrypt data sent to server |

### Building the Secure Tunnel
- Server + client use the **key pair** + a chosen **cipher suite** (within TLS) to set up an **encrypted tunnel**
- Even if someone knows the **public key**, they **cannot decrypt** traffic without the **private key**
- Result: communications **can't be read or altered** by a third party

---

## What the User Sees
- URL starts with `https://`
- Browser shows a **padlock icon** in the address bar
  - Confirms: server's certificate is **trusted** + connection is **encrypted**
- Websites can be configured to:
  - **Require** HTTPS
  - **Reject or redirect** plain HTTP requests

---

## Quick Summary
- HTTP = insecure; **TLS** (modern successor to SSL) = adds encryption + authentication
- **HTTPS** = HTTP secured by TLS, uses **port 443**
- "S" at the **end** of a protocol name = secured by SSL/TLS (HTTPS, FTPS, SMTPS, etc.)
- **DTLS** = TLS over UDP, common in VPNs
- HTTPS relies on a **digital certificate** (from a trusted CA) + **public/private key pair**
- Browser shows a **padlock** to confirm a trusted, encrypted connection

