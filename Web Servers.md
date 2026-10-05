
## Web Servers Overview
- A **web server** provides client access using **HTTP** or its secure version **HTTPS**
- Websites/web apps = most common network service
- Not limited to static pages - huge range of uses

---

## HTTP (HyperText Transfer Protocol)

### Basics
- Lets clients (**browsers**) request resources from an **HTTP server**
- Client connects using **TCP port 80** (default)
- Client sends a **GET** request
- Server responds with:
  - The requested data, OR
  - An **error code**

### Example Response Info (from browser dev tools)
- Status: **200 OK**
- Version: **HTTP/2**
- Headers include: cache-control, content-type, content-length, date, expires, etc.

---

## HTML and Web Forms

### HTML
- HTTP usually serves **HTML** pages
- HTML = plain text files with **coded tags** for formatting
- Browser **interprets tags** to display text, images, sound, etc.
- Supports **hyperlinks** to other documents

### Submitting Data
- HTTP has a **POST** method -> lets users **submit data** from client to server (e.g., forms)

### Web Applications
- HTTP server functionality can be extended with:
  - **Scripting**
  - **Programmable features**
  - = **Web applications** (not just static pages)

---

## URLs (Uniform Resource Locators)

### Purpose
- Addressing scheme to access Internet resources
- Example: `http://www.microsoft.com`

### URL Structure
| Part | Description |
|------|--------------|
| **Protocol** | Access method/service type (e.g., http, https) |
| **Host location** | Usually an **FQDN** (not case-sensitive); can also be an IP address (IPv6 must use `[brackets]`) |
| **File path** | Directory/file name of the resource (case-sensitivity depends on server config) |

### Example Breakdown
```

[https://store.comptia.org/bundles/aplus.html](https://store.comptia.org/bundles/aplus.html)

```

| Part        | Value                 |
| ----------- | --------------------- |
| Protocol    | `https://`            |
| FQDN (host) | `store.comptia.org`   |
| File path   | `/bundles/aplus.html` |

---

## Web Server Deployment

### Common Setups
- Organizations often **lease a web server** or **space on a server** from an ISP
- Larger orgs with their own datacenters may **host websites themselves**

### Private Web Deployments
| Term | Meaning |
|------|---------|
| **Intranet** | Private network using web tech, **local access only** |
| **Extranet** | Private network using web tech, but allows **remote access** too |

---

## Quick Summary
- **HTTP** = protocol for requesting/serving web resources (port 80 default)
- **GET** = request data; **POST** = submit data to server
- **HTML** = the markup language browsers interpret to display pages
- **URL structure** = Protocol + FQDN/IP (host) + File path
- Web servers can be **leased** (small orgs) or **self-hosted** (large orgs)
- **Intranet** = internal-only; **Extranet** = internal + remote access

