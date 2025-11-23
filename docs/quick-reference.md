# CNSP Quick Reference Guide

A condensed cheat sheet for last-minute review before the exam.

---

## 🔢 Common Ports & Protocols

| Port | Protocol | Service | Notes |
|------|----------|---------|-------|
| 20/21 | TCP | FTP | File Transfer Protocol |
| 22 | TCP | SSH | Secure Shell |
| 23 | TCP | Telnet | Unencrypted remote access |
| 25 | TCP | SMTP | Simple Mail Transfer Protocol |
| 53 | UDP | DNS | Domain Name System (queries) |
| 53 | TCP | DNS | Zone transfers |
| 80 | TCP | HTTP | **No encryption by default** |
| 110 | TCP | POP3 | Post Office Protocol |
| 111 | TCP | RPC | Remote Procedure Call |
| 143 | TCP | IMAP | Internet Message Access Protocol |
| 161/162 | UDP | SNMP | Simple Network Management Protocol |
| 389 | TCP | LDAP | Lightweight Directory Access Protocol |
| 443 | TCP | HTTPS | HTTP Secure |
| 445 | TCP | SMB | Server Message Block |
| 1433/1434 | TCP/UDP | MSSQL | Microsoft SQL Server |
| 3306 | TCP | MySQL | MySQL Database |
| 3389 | TCP | RDP | Remote Desktop Protocol |
| 5432 | TCP | PostgreSQL | PostgreSQL Database |

**Total Ports**: 65,536 (0-65535)

---

## 🔍 Scan Responses

### TCP Scan Responses

| Scenario | Response |
|----------|----------|
| Open port (no firewall) | SYN-ACK |
| Closed port (no firewall) | RST-ACK |
| Closed port (with firewall) | No response OR RST-ACK |
| Filtered port | No response |

### UDP Scan Responses

| Scenario | Response |
|----------|----------|
| Open port (any) | No response |
| Closed port (no firewall) | ICMP Destination Unreachable |
| Closed port (with firewall) | No response |

---

## 🪟 Windows Commands

```cmd
# Display local administrators group
net localgroup administrators

# Add user to local group
net localgroup GroupName UserName /add

# Add domain group to local group
net localgroup LocalGroup DomainGroup /add

# Add user to domain admins
net group "Domain Admins" UserName /add /domain

# Establish null session
NET USE \\hostname\ipc$ "" /u:""

# Verify Kerberos tickets
klist
```

**Important**:
- RID 500 = Administrator account
- NTDS.DIT = Active Directory database
- KRBTGT account = Required for Golden Ticket
- TGT = Required for Silver Ticket

---

## 🐧 Linux File Permissions

### Permission Notation
```
-rwxr-xr-x  = Regular file
drwxr-xr-x  = Directory
-rwsr-xr-x  = SUID set (s in user position)
-rwxr-sr-x  = SGID set (s in group position)
```

### Special Permissions
- **SUID**: Runs with owner's permissions (e.g., `/usr/bin/passwd`)
- **SGID**: Runs with group's permissions
- **Sticky Bit**: Only owner can delete files

### Important Paths
- `/etc/shadow` = Password hashes
- `/etc/passwd` = User account info
- `/mnt` = Temporary-mounted filesystems

### Commands
```bash
# Change MAC address
ifconfig eth0 hw ether AA:BB:CC:DD:EE:FF

# Enumerate RPC services
rpcinfo -p <hostname>
```

**Daemon processes**: Execute in **user space** (not kernel space)

**Dotfiles**: Hidden files (start with `.`)

---

## 🔐 Cryptography

### Encryption Types
- **Symmetric**: Same key for encryption/decryption (AES, DES)
- **Asymmetric**: Public/private key pairs (RSA, ECC)

### Key Exchange
- **Diffie-Hellman**: Secure key exchange algorithm

### Hashing Algorithms
| Hash Prefix | Algorithm |
|-------------|-----------|
| `$2a$` | Bcrypt (Blowfish) |
| `$1$` | MD5 |
| `$5$` | SHA-256 |
| `$6$` | SHA-512 |

### SSL/TLS Versions
| Version | Status |
|---------|--------|
| SSLv2 | ❌ Unsafe |
| SSLv3 | ❌ Unsafe |
| TLSv1.0 | ❌ Unsafe |
| TLSv1.1 | ❌ Unsafe |
| TLSv1.2 | ✅ Safe |
| TLSv1.3 | ✅ Safe |

### SSH Keys
- **Public key**: Uploaded to server
- **Private key**: Used by end-user for authentication

### Other Terms
- **TLS**: Transport Layer Security
- **S/MIME**: Secure/Multipurpose Internet Mail Extensions
- **Substitution cipher**: Each letter replaced by another

---

## 🌐 DNS

### DNS Record Types
- **A**: IPv4 address
- **AAAA**: IPv6 address
- **MX**: Mail exchange
- **TXT**: Text record
- **SRV**: Service record
- **NAPTR**: Name authority pointer
- **PTR**: Pointer record

### DNS Zone Transfer
```bash
# Perform zone transfer
dig @nameserver domain.com axfr

# Uses TCP port 53 (not UDP)
```

### DNS Cache Poisoning
**Risk**: Attacker redirects traffic to malicious IP by manipulating DNS cache

---

## 🔌 SMB Protocol

| Version | Features | Vulnerabilities |
|---------|----------|-----------------|
| SMBv1 | Basic file sharing | EternalBlue (MS17-010/WannaCry) |
| SMBv2 | Improved performance | EternalBlue (MS17-010) |
| SMBv3 | **Encryption support** | More secure |

---

## 📡 SNMP

**Default Community Strings**:
- Read-only: `public`
- Read/write: `private`

**Enumeration Tool**: `snmpwalk`

**MIB**: Management Information Base (managed by SNMP)

**Security Risk**: Default community strings allow unauthorized access

---

## 🎯 Attack Types

### Online Attacks
- Brute Force
- Dictionary Attack
- Password Spraying
- Credential Stuffing

### Offline Attacks
- Rainbow Table Attack
- Hash Cracking

### Network Attacks
- **DDoS**: Distributed Denial of Service
- **ICMP Attacks**: Ping flood, Smurf, Ping of Death
- **DNS Cache Poisoning**: Redirect traffic
- **Address Spoofing**: TCP resistant if implemented correctly

### Not DDoS
- Brute Force (single source)

---

## 🔧 Network Segmentation Bypass

Techniques:
- DNS tunneling
- VLAN hopping
- Covert channels

---

## 📊 Subnetting Quick Reference

| CIDR | Subnet Mask | Hosts |
|------|-------------|-------|
| /8 | 255.0.0.0 | 16,777,214 |
| /16 | 255.255.0.0 | 65,534 |
| /18 | 255.255.192.0 | 16,382 |
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /30 | 255.255.255.252 | 2 |

---

## 🌍 IPv6

**Octets**: 16 octets (128 bits)

**Format**: Eight groups of four hexadecimal digits

---

## 🛡️ Authentication vs Authorization

- **Authentication**: Providing and validating identity (Who are you?)
- **Authorization**: Granting or denying access to resources (What can you do?)

---

## 🧪 Testing Tools

**EICAR File**: Test antivirus response (not actual malware)

---

## 💡 Quick Tips

1. **Read questions carefully**: Look for "not," "except," "best"
2. **Eliminate wrong answers**: Narrow down choices
3. **Trust your preparation**: First instinct usually correct
4. **Manage time**: 1 minute per question, 10 minutes for review
5. **Flag difficult questions**: Come back if time permits

---

## 📖 Related Resources

- [Full Syllabus](syllabus.md) - Detailed topic breakdown
- [Practice Questions](practice-questions.md) - Test your knowledge
- [My Experience](my-experience.md) - Exam tips and insights
- [Study Materials](study-materials.md) - Preparation resources

---

**Pro Tip**: Print this page and review it the night before your exam!
