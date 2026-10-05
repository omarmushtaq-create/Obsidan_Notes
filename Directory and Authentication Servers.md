
## The Need for Access Control
- **DHCP** = gets IP config | **DNS** = resolves names
- But networks also need to **authenticate/authorize** users before they can access fileshares, mail servers, etc.

### Simple vs Enterprise Access Control
| Setup                  | Method                                                    |
| ---------------------- | --------------------------------------------------------- |
| **Windows Workgroup**  | Simple shared password                                    |
| **Enterprise Network** | **Directory servers** - centralized user account database |

### Single Sign-On (SSO)
- Enterprise protocols let a user **authenticate once**
- Then get authorization across **all compatible servers** on the network
- = **Single Sign-On (SSO)**

---

## LDAP (Lightweight Directory Access Protocol)

### What is a Directory?
- A **directory** = type of database
  - **Object** = like a record (e.g., a user)
  - **Attribute** = like a field (info about that object)
- Most directories follow the **X.500 standard**

### LDAP Basics
- **LDAP** = TCP/IP protocol to **query and update** an X.500-style directory
- Used by: **Windows Active Directory**, **OpenLDAP**

### Ports
| Port | Security |
|------|----------|
| TCP/UDP 389 | Default (unencrypted) |
| TCP 636 | **LDAPS** (secured via TLS) |

---

## AAA (Authentication, Authorization, and Accounting)

### Why AAA?
- Clients can connect via many access devices: switches, APs, VPN servers
- Storing directory/auth info on **every** device = more processing, more storage, **bigger security risk**
- Solution: **AAA server** = centralizes authentication for all access devices

### AAA Components
| Term | Role |
|------|------|
| **Supplicant** | The device requesting access (e.g., user's laptop) |
| **NAS / NAP** (Network Access Server/Point) | The access device (switch, AP, VPN gateway) - aka "AAA client" or "authenticator" |
| **AAA server** | The actual authentication server on the local network |

> With AAA, access devices (NAS) **don't store credentials** - they just **relay** the authentication request to the AAA server.

---

## RADIUS vs TACACS+

| Protocol | Port | Commonly Used For |
|----------|------|----------------------|
| **RADIUS** | TCP/UDP 1812/1813 | Authenticating **users** to a network |
| **TACACS+** | TCP/49 | Authenticating **devices** (routers, switches) |

---

## RADIUS Authentication Process (Step-by-Step)

| Step | What Happens |
|------|----------------|
| 1 | RADIUS server + client (NAS) pre-share a **secret** |
| 2 | Supplicant connects to the network |
| 3 | Switch tells supplicant to authenticate, **blocks other traffic** |
| 4 | Supplicant sends its **credentials** |
| 5 | Switch **forwards** credentials to the RADIUS server |
| 6 | RADIUS server **validates** the credentials |
| 7 | RADIUS server sends back **Access Accept** |
| 8 | Switch **opens** the network for normal traffic |

---

## Quick Summary
- **LDAP** = protocol to query/update a directory (user accounts, etc.) - port 389 (636 secure)
- **SSO** = authenticate once, access everything you're authorized for
- **AAA** = centralizes authentication across all access devices (supplicant -> NAS -> AAA server)
- **RADIUS** = authenticates **users** (port 1812/1813)
- **TACACS+** = authenticates **devices** like routers/switches (port 49)

