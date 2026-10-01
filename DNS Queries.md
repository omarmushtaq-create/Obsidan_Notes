
# DNS Name Resolution Process

## Starting the Query
- Client types an FQDN into browser (e.g., `www.515web.net`)
- Client app = **"stub resolver"**
- Stub resolver first checks its **local cache**
- If no cached match -> query is forwarded to the **local DNS server**
- Local DNS server address comes from **TCP/IP configuration**
- Communication with DNS server happens over **port 53**

---

## The Resolution Process (Step-by-Step)

### Step 1: Client Queries
- Client asks its **Local Name Server** for `www.515web.net`

### Step 2: Local Server Has No Answer
- Local Name Server is **not authoritative** for `515web.net`
- No cached record either
- Configured to do **recursive querying** -> contacts a **Root Server** (using a pre-configured list of root server IPs)

### Step 3: Root Server Responds
- Root server is **not authoritative** for the record either
- BUT it knows which server handles **.net** domains
- Returns the address of the **.net TLD Name Server**

### Step 4: .net TLD Server Responds
- Local server asks the **.net TLD Name Server**
- TLD server is **not authoritative** either
- BUT it knows the **authoritative name server for 515web.net**
- Returns that info

### Step 5: Authoritative Server Responds
- Local server asks the **Authoritative Name Server** for `515web.net`
- This server **IS authoritative** for the domain
- Returns the actual requested record: **www.515web.net's IP address**

### Step 6: Local Server Caches and Replies
- Local Name Server **caches** the record (so it doesn't have to repeat this whole process next time)
- Sends the answer back to the client

### Step 7: Client Gets the Answer
- Client now has the **IP address** for `www.515web.net`
- Client also **caches** this record locally

---

## Quick Visual Summary (Chain of "Who Do I Ask Next")
```

Client  
-> Local Name Server (no cache, not authoritative)  
-> Root Server (not authoritative, but knows .net TLD server)  
-> .net TLD Server (not authoritative, but knows 515web.net's server)  
-> Authoritative Name Server (HAS the answer)  
<- Local Name Server caches answer  
<- Client receives + caches answer

```

> This is called **recursive querying**: the local server does all the legwork, chasing the answer through root -> TLD -> authoritative server, rather than making the client do each lookup itself.

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