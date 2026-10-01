
## TXT Records
- **TXT record** = stores **free-form text** data for a domain
- A domain can have **multiple TXT records**
- Most common use: **email verification** and **anti-spam** protection

---

## SPF (Sender Policy Framework)

### Purpose
- Identifies **which servers are allowed to send email** for a domain
- Published as a **TXT record**
- **Only one SPF record allowed per domain**

### What It Can Specify
| Tag | Meaning | Action for Unauthorized Senders |
|-----|---------|-----------------------------------|
| `-all` | Hard fail | **Reject** the mail |
| `~all` | Soft fail | **Flag** the mail (mark as suspicious) |
| `+all` | Pass | **Accept** the mail (not recommended - too permissive) |

---

## DKIM (DomainKeys Identified Mail)

### Purpose
- Uses **cryptography** to verify the **source server** of an email
- Can **replace or work alongside** SPF

### How It Works
1. Organization uploads a **public encryption key** as a **TXT record** in DNS
2. Receiving mail servers use this key to **verify authenticity** of the message
3. Confirms the message really came from an **authorized server** for that domain

---

## DMARC (Domain-Based Message Authentication, Reporting, and Conformance)

### Purpose
- Makes sure **SPF and DKIM** are being used **effectively**
- Published as a **DNS TXT record**
- Can use **SPF, DKIM, or both**

### What It Adds
- A **policy mechanism** for what to do when authentication fails:
  - **Flag**
  - **Quarantine**
  - **Reject**
- A **reporting mechanism**: lets recipients report authentication failures back to the sender

---

## Quick Comparison Table

| Protocol | What It Checks | Published As | Key Feature |
|----------|------------------|----------------|----------------|
| **SPF** | Which servers can send mail for the domain | TXT record | List of authorized senders + action (reject/flag/accept) |
| **DKIM** | Cryptographic proof message is authentic | TXT record (public key) | Digital signature verification |
| **DMARC** | Makes sure SPF/DKIM are enforced properly | TXT record | Policy (flag/quarantine/reject) + failure reporting |

---

## Quick Summary
- **TXT record** = general-purpose text storage in DNS, often used for email security
- **SPF** = whitelist of servers allowed to send mail for a domain
- **DKIM** = cryptographic signature to prove mail authenticity
- **DMARC** = enforces SPF/DKIM compliance + defines failure handling + reporting
- All three work together to **prevent spoofed/spam email**
