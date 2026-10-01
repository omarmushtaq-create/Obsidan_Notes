

## Starting the Query
- Client types an FQDN into browser (e.g., `www.515web.net`)
- Client app = **"stub resolver"**
- Stub resolver first checks its **local cache**
- If no cached match -> query is forwarded to the **local DNS server**
- Local DNS server address comes from **TCP/IP configuration**
- Communication with DNS server happens over **port 53**




---

## Key Terms
| Term | Meaning |
|------|---------|
| **Stub resolver** | The client-side app/component that starts the DNS query |
| **Recursive query** | Local server keeps asking other servers until it gets a final answer |
| **Authoritative server** | The server that actually holds the real record for a domain |
| **Caching** | Storing the answer temporarily so future queries are faster |

---

## Quick Summary
- DNS resolution = chain of lookups: **Local -> Root -> TLD -> Authoritative**
- Only the **authoritative server** has the real answer
- Root and TLD servers just **point you in the right direction**
- Once found, the answer is **cached** at both the local server and the client
- All DNS communication uses **port 53**

![[Pasted image 20261001171936.png]]