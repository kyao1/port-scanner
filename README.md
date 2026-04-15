# 🔍 Simple Port Scanner

A beginner-friendly Python port scanner that checks which ports are open on a target system and identifies the services running on them.

> **Project by Konan Achille Yao** | B.S. Computer Science @ IU Indianapolis (Luddy School)

---

## ⚠️ Legal Notice
Only scan systems **you own** or have **explicit written permission** to scan. Unauthorized port scanning may be illegal in your jurisdiction.

---

## What It Does

Port scanning is one of the first steps in network security auditing. This tool checks 17 of the most critical ports and tells you exactly what's exposed — the same way security professionals assess a network.

```
╔══════════════════════════════════════╗
║         SIMPLE PORT SCANNER          ║
║         by Konan Achille Yao          ║
╚══════════════════════════════════════╝

  NOTE: Only scan systems you own or have permission to scan.

  Enter target IP or hostname: scanme.nmap.org

  Resolving host... 45.33.32.156
  Starting scan of 17 common ports...

  closed  port 21     FTP        (File Transfer)
  OPEN    port 22     SSH        (Secure Shell)
  closed  port 23     Telnet     (Unencrypted remote login - DANGEROUS)
  closed  port 25     SMTP       (Email sending)
  closed  port 53     DNS        (Domain Name System)
  OPEN    port 80     HTTP       (Web - unencrypted)
  ...

  SCAN COMPLETE
  Open      : 2 port(s) found
  Duration  : 4.31 seconds

  OPEN PORTS SUMMARY
  ▶  22     SSH        (Secure Shell)
  ▶  80     HTTP       (Web - unencrypted)

  ✔  No obviously dangerous ports detected.
```

---

## Ports Checked

| Port | Service | Risk |
|------|---------|------|
| 21 | FTP | Medium |
| 22 | SSH | Low |
| 23 | Telnet | 🔴 High |
| 25 | SMTP | Medium |
| 53 | DNS | Low |
| 80 | HTTP | Low |
| 139 | NetBIOS | 🔴 High |
| 443 | HTTPS | Low |
| 445 | SMB | 🔴 High |
| 3306 | MySQL | 🔴 High |
| 3389 | RDP | 🔴 High |
| + more | ... | ... |

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/kyao1/port-scanner.git
cd port-scanner

# Run it
python3 port_scanner.py

# Safe target to test on (publicly authorized for scanning)
# Enter: scanme.nmap.org
```

No external libraries needed — uses Python's built-in `socket` module only.

---

## What I Learned

- How TCP connections work at the socket level
- What ports and services are and why they matter in security
- How to use Python's `socket` module for network programming
- Why certain ports (23, 445, 3389) are high-risk when exposed
- How to write tools that security professionals actually use

---

## Skills Demonstrated

`Python` · `socket module` · `Networking` · `TCP/IP` · `Cybersecurity` · `Port scanning` · `Risk assessment`

---

## Author

**Konan Y.**
- LinkedIn: [linkedin.com/in/konanyao](https://linkedin.com/in/konanyao)
- CompTIA A+ certified | A.S. Cybersecurity & Information Assurance | IU Indianapolis CS student
