
## Resource Sharing Basics
- Core network function = **shared access to disks/printers**
- Uses **client/server** model:
  - **Server** = hosts the disk/printer
  - **Client** = machine accessing it
- A shared server disk = **file share**
- Can be implemented via:
  - Proprietary protocols (e.g., **File and Print Services for Windows Networks**)
  - TCP/IP protocols (e.g., **FTP**)

---

## SMB (Server Message Block)

### Basics
- Application protocol behind **file/printer sharing on Windows networks**
- Runs over **TCP port 445**
- Current version: **SMB3**

### Security Note
- **SMB1** = serious security vulnerabilities -> **disabled by default** on modern Windows

### Cross-Platform Support
- **Samba** = software suite that adds SMB support to **Linux/UNIX** and **NAS** devices
  - Lets Windows clients access a Linux host like a normal Windows file/print server

### Naming Note
- SMB is sometimes called **CIFS (Common Internet File System)**
  - Technically, CIFS should only refer to a **specific SMBv1 dialect**, not SMB in general

---

## Print Servers
- Manage **printers and print jobs** across the network
- Can be **hardware or software** based
- Benefits:
  - **Centralized management** -> more efficient handling of high print volumes
  - Can **queue** print jobs
  - Can **hold jobs** until a user manually releases them (prevents unclaimed prints sitting in the printer)

---

## NetBIOS / NetBT

### History
- Earliest Windows networks used **NetBIOS** instead of TCP/IP
- NetBIOS let computers:
  - Address each other **by name**
  - Establish sessions for protocols like **SMB**

### NetBT (NetBIOS over TCP/IP)
- As TCP/IP became standard, NetBIOS was adapted to run over TCP/UDP

| Port | Purpose |
|------|---------|
| UDP/137 | Name services |
| UDP/138 | UDP connections |
| TCP/139 | TCP session services |

### Current Status
- **Obsolete** - modern networks use IP/TCP/UDP/DNS instead
- **Should be disabled** on most networks (security risk)
- Only needed for supporting **Windows versions older than Windows 2000**

---

## FTP (File Transfer Protocol)

### Basics
- Lets clients **upload/download files** from a server
- Commonly used to **upload files to websites**

### Ports
| Port                 | Purpose                          |
| -------------------- | -------------------------------- |
| TCP/21               | Establish/maintain connection    |
| TCP/20               | Data transfer (**active mode**)  |
| Server-assigned port | Data transfer (**passive mode**) |

### Security Warning
- **Plain FTP = unencrypted** -> **high security risk**
  - Passwords sent in **plaintext**
- Secure alternatives (more widely used today):
  - **FTPS** (FTP-Secure)
  - **SFTP** (FTP over SSH)

---

## Quick Summary Table

| Protocol | Purpose | Port(s) | Notes |
|----------|---------|---------|-------|
| **SMB** | Windows file/print sharing | TCP/445 | SMB3 = current, SMB1 disabled (insecure) |
| **NetBT** | Legacy name resolution/sessions | UDP/137, UDP/138, TCP/139 | Obsolete, should be disabled |
| **FTP** | File upload/download | TCP/21 (control), TCP/20 or dynamic (data) | Unencrypted - use FTPS/SFTP instead |

