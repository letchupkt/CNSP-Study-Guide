# CNSP Exam Syllabus & Topics

The CNSP exam covers a wide range of network security fundamentals. Below is a detailed breakdown of the key knowledge domains.

## 📚 Core Knowledge Domains

### 1. TCP/IP & Networking Fundamentals

#### OSI Model
- Understanding the 7 layers of the OSI model
- How data flows through each layer
- Protocols associated with each layer

#### IP Addressing
- **IPv4**: Address classes, subnetting, CIDR notation
- **IPv6**: Address structure, octets (16 octets in IPv6)
- Subnet mask calculations (e.g., /18 = 255.255.192.0)
- Network and host portions of IP addresses

#### Network Devices
- Routers, Switches, Hubs
- How they operate at different OSI layers
- Security implications of each device type

#### Protocols
- **TCP**: Three-way handshake (SYN, SYN-ACK, ACK)
- **UDP**: Connectionless protocol characteristics
- **ICMP**: Ping, error messages, attacks
- Port numbers: 65,536 total TCP/UDP ports (0-65535)
- Common service ports (HTTP: 80, HTTPS: 443, SSH: 22, MSSQL: 1433/1434)

---

### 2. Network Discovery, Scanning & Fingerprinting

#### Scanning Tools
- **Nmap**: Port scanning, service detection, OS fingerprinting
- **Wireshark**: Packet capture and analysis
- Understanding scan responses:
  - Open TCP port: SYN-ACK response
  - Closed TCP port (no firewall): RST-ACK response
  - Closed TCP port (with firewall): No response or RST-ACK
  - Open UDP port: No response
  - Closed UDP port (no firewall): ICMP Destination Unreachable

#### Network Discovery
- Host discovery techniques
- Service enumeration
- Banner grabbing
- Network mapping

#### DNS Operations
- DNS record types: A, AAAA, MX, TXT, SRV, NAPTR, PTR
- **DNS Zone Transfer**: Uses TCP port 53
- Command: `dig @nameserver domain.com axfr`
- DNS cache poisoning attacks and risks

---

### 3. Active Directory & Windows Security

#### Active Directory Basics
- **KRBTGT Account**: Used for Golden Ticket attacks
- **Kerberos Tickets**: TGT (Ticket-Granting Ticket), Service Tickets
- **Silver Ticket**: Requires TGT
- **Golden Ticket**: Requires KRBTGT account hash
- **Klist**: Built-in Windows utility to verify Kerberos tickets

#### Windows File System & Registry
- **Registry Keys**: HKEY_LOCAL_MACHINE, HKEY_CURRENT_USER, etc.
- **SAM Database**: Stores local user account hashes
- **NTDS.DIT**: Active Directory database file
- Important file paths and their purposes

#### Windows Commands
- `net localgroup administrators` - Display local admin group
- `net localgroup GroupName UserName /add` - Add user to local group
- `net group "Domain Admins" UserName /add /domain` - Add domain admin
- `NET USE \\hostname\ipc$ "" /u:""` - Establish null session

#### Windows Security
- **RID 500**: Administrator account
- Common vulnerabilities in Windows services
- Account and group management

---

### 4. Linux & Unix Security

#### File System Structure
- **/etc/shadow**: Password hashes storage
- **/etc/passwd**: User account information
- **/mnt**: Temporary-mounted filesystems
- Other critical directories

#### File Permissions
- **SUID (Set User ID)**: `-rwsr-xr-x` (s in user execute position)
- **SGID (Set Group ID)**: `-rwxr-sr-x` (s in group execute position)
- Example SUID program: `/usr/bin/passwd`
- Understanding permission notation (rwx)

#### Linux Commands
- `ifconfig eth0 hw ether AA:BB:CC:DD:EE:FF` - Change MAC address
- File permission management
- User and group administration

#### Daemon Processes
- Execute in **user space** (not kernel space)
- Background service management
- Security implications

#### Dotfiles
- Files beginning with `.` (dot)
- **Hidden files** in Linux
- Configuration files

---

### 5. Cryptography & Authentication

#### Encryption Types
- **Symmetric Encryption**: Same key for encryption and decryption
- **Asymmetric Encryption**: Public/private key pairs
- Use cases for each type

#### Key Exchange
- **Diffie-Hellman**: Algorithm for secure key exchange
- How it prevents man-in-the-middle attacks

#### Hashing Algorithms
- **Bcrypt**: Hash begins with `$2a$` (also known as Blowfish)
- **SHA family**: SHA-1, SHA-256, SHA-512
- **MD5**: Weak, deprecated
- Rainbow table attacks (offline attack)

#### SSL/TLS
- **TLS**: Transport Layer Security
- **S/MIME**: Secure/Multipurpose Internet Mail Extensions
- **Unsafe versions**: SSLv2, SSLv3, TLSv1.0, TLSv1.1
- **Safe versions**: TLSv1.2, TLSv1.3
- Port 443 for HTTPS
- Certificate expiration doesn't break TLS encryption

#### SSH Authentication
- **Public key**: Uploaded to the server
- **Private key**: Used by end-user for authentication
- Key-based vs. password authentication

#### Classical Cryptography
- **Substitution cipher**: Each letter replaced by another letter

---

### 6. Network Services & Threat Mitigation

#### Common Services & Ports
- **HTTP**: 80/TCP (no encryption by default)
- **HTTPS**: 443/TCP
- **SSH**: 22/TCP
- **DNS**: 53/UDP (queries), 53/TCP (zone transfers)
- **MSSQL**: 1433/TCP, 1434/TCP, 1434/UDP
- **RPC**: 111/TCP (use `rpcinfo -p` to enumerate)
- **SNMP**: 161/UDP, 162/UDP

#### SNMP Security
- **Default community strings**:
  - Read-only: `public`
  - Read/write: `private`
- **MIB**: Management Information Base (managed by SNMP)
- Use `snmpwalk` to query devices
- Security risks of default community strings

#### SMB Protocol
- **SMBv1 & SMBv2**: Vulnerable to EternalBlue (MS17-010/WannaCry)
- **SMBv3**: Introduced encryption support
- Security improvements across versions

#### Attack Types
- **DDoS Attacks**: Distributed Denial of Service
- **ICMP Attacks**: Ping floods, Smurf attacks
- **DNS Cache Poisoning**: Redirecting traffic to malicious sites
- **Address Spoofing**: TCP is resistant if implemented correctly
- **Brute Force**: Not a DDoS attack (single source)

#### Network Segmentation Bypass
- DNS tunneling
- VLAN hopping
- Covert channels

#### Testing Tools
- **EICAR file**: Test antivirus response (not malware)

---

## 📊 Exam Weight Distribution

While The SecOps Group doesn't publish exact percentages, expect:

- **Networking Fundamentals**: ~25-30%
- **Operating System Security**: ~20-25%
- **Cryptography**: ~15-20%
- **Network Services**: ~15-20%
- **Attacks & Mitigation**: ~15-20%

---

## 🎯 Study Tips by Domain

### For TCP/IP & Networking
- Practice subnetting calculations
- Memorize common port numbers
- Understand TCP vs. UDP differences
- Know scan response types

### For Windows Security
- Practice `net` commands in a lab
- Understand AD attack vectors
- Know file system paths

### For Linux Security
- Set up a Linux VM for hands-on practice
- Practice file permission commands
- Understand SUID/SGID implications

### For Cryptography
- Understand when to use symmetric vs. asymmetric
- Know hash algorithm identifiers
- Understand SSL/TLS version security

### For Network Services
- Know default ports and protocols
- Understand service vulnerabilities
- Practice with enumeration tools

---

## 📖 Next Steps

- Review [Study Materials](study-materials.md) for resources
- Practice with [Sample Questions](practice-questions.md)
- Set up a lab environment for hands-on practice
- Read [My Experience](my-experience.md) for exam tips
