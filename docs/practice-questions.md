# CNSP Practice Questions

This document contains practice questions similar to those found on the actual CNSP exam. All questions are multiple choice and cover the key domains tested.

---

## 📝 Practice Questions

### Networking Fundamentals

**Q1: Which of the following services do not encrypt its traffic by default?**
- A. DNS ✅
- B. HTTPS
- C. SSH
- D. SFTP

**Q2: How many usable TCP/UDP ports are there?**
- A. 65536 ✅
- B. 65535
- C. 1024
- D. 49152

**Q3: What ports does a MSSQL server typically use?**
- A. 3306/TCP
- B. 1433/TCP, 1434/TCP, and 1434/UDP ✅
- C. 5432/TCP
- D. 1521/TCP

**Q4: The port used by HTTPS protocol is ________________.**
- A. 443 ✅
- B. 80
- C. 8080
- D. 8443

**Q5: What will be the subnet mask for 192.168.0.1/18?**
- A. 255.255.255.0
- B. 255.255.0.0
- C. 255.255.128.0
- D. 255.255.192.0 ✅

**Q6: How many octets are there in an IPv6 address?**
- A. 16 ✅
- B. 8
- C. 4
- D. 32

---

### TCP/UDP Responses

**Q7: What is the response from an open TCP port which is not behind a firewall?**
- A. A SYN packet
- B. A RST and an ACK packet
- C. A SYN and an ACK packet ✅
- D. No response

**Q8: What is the response from a closed TCP port which is not behind a firewall?**
- A. A SYN and an ACK packet
- B. No response
- C. A RST and an ACK packet ✅
- D. ICMP Destination Unreachable

**Q9: What is the response from a closed TCP port which is behind a firewall?**
- A. A SYN and an ACK packet
- B. A RST and an ACK packet ✅
- C. ICMP Destination Unreachable
- D. No response ✅

*Note: Both B and D can be correct depending on firewall configuration*

**Q10: What is the response from an open UDP port which is not behind a firewall?**
- A. ICMP Destination Unreachable
- B. No response ✅
- C. UDP ACK packet
- D. UDP SYN packet

**Q11: What is the response from a closed UDP port which is not behind a firewall?**
- A. ICMP message showing Destination Unreachable ✅
- B. No response
- C. UDP RST packet
- D. UDP ACK packet

**Q12: What is the response from an open UDP port which is behind a firewall (port is open on the firewall)?**
- A. ICMP Destination Unreachable
- B. No response ✅
- C. UDP ACK packet
- D. UDP confirmation packet

---

### Windows Security

**Q13: Which of the following represents a valid Windows Registry Key?**
- A. HKEY_LOCAL_MACHINE ✅
- B. HKEY_SYSTEM_ROOT
- C. HKEY_ADMIN_USER
- D. HKEY_NETWORK_CONFIG

**Q14: On a Microsoft Windows Operating system, what does the following command do? `net localgroup administrators`**
- A. Creates a new administrators group
- B. Displays the local administrators group on the computer ✅
- C. Deletes the administrators group
- D. Adds a user to the administrators group

**Q15: On a Microsoft Windows Operating system, what does the following command do? `net localgroup Sales Sales_domain /add`**
- A. Creates a new local group called Sales
- B. Add a domain group to the local group Sales ✅
- C. Removes Sales_domain from Sales group
- D. Renames the Sales group

**Q16: Which of the following commands will work on a Microsoft operating system to add a new domain admin user?**
- A. net group "Domain Admins" John /add /domain ✅
- B. net localgroup "Domain Admins" John /add
- C. net user John /add /admin
- D. net domain John /add /admin

**Q17: What RID is given to an Administrator account on a MS Windows machine?**
- A. 501
- B. 500 ✅
- C. 1000
- D. 0

**Q18: How would you establish a null session to a windows host from a windows command prompt?**
- A. NET USE \\hostname\ipc$
- B. NET USE \\hostname\admin$
- C. NET USE \\hostname\c$
- D. NET USE \\hostname\ipc$ "" /u:"" ✅

---

### Active Directory & Kerberos

**Q19: What user account is required to create a Golden Ticket in Active Directory?**
- A. Administrator
- B. Domain Admin
- C. Enterprise Admin
- D. KRBTGT account ✅

**Q20: Which built-in Windows utility can be used to verify the validity of a Kerberos ticket?**
- A. Klist ✅
- B. Kerbcheck
- C. Ticketview
- D. Netstat

**Q21: Which Kerberos ticket is required to generate a Silver Ticket?**
- A. Golden Ticket
- B. Ticket-Granting Ticket ✅
- C. Service Ticket
- D. Authentication Ticket

**Q22: Which of the following file is the Active Directory database file?**
- A. SAM
- B. SYSTEM
- C. SECURITY
- D. NTDS.DIT ✅

---

### Linux/Unix Security

**Q23: Where are the password hashes stored in the Linux file system?**
- A. /etc/passwd
- B. /etc/security
- C. /etc/shadow ✅
- D. /etc/hash

**Q24: What kind of files are "Dotfiles" in a Linux-based architecture?**
- A. System files
- B. Executable files
- C. Configuration files
- D. Hidden Files ✅

**Q25: Which of the following files has the SUID permission set?**
- A. myfile (-rwxr-xr-x)
- B. myprogram (-rwsr-xr-x) ✅
- C. myfile (-rwxr-sr-x)
- D. myprogram (-rwxrwxrwx)

**Q26: Which of the following files has the SGID permission set?**
- A. myfile (-rwxr-sr-x) ✅
- B. myprogram (-rwsr-xr-x)
- C. myfile (-rwxr-xr-x)
- D. myprogram (-rwxrwxrwx)

**Q27: Which of the following is an example of a SUID program?**
- A. /bin/ls
- B. /bin/cat
- C. /usr/bin/passwd ✅
- D. /usr/bin/grep

**Q28: In the context of a Unix-based system where does a daemon process execute in the memory?**
- A. Kernel space
- B. User space ✅
- C. System space
- D. Protected space

**Q29: Which is the correct command to change the MAC Address for an Ethernet Adapter in a Unix-based system?**
- A. ifconfig eth0 hw ether AA:BB:CC:DD:EE:FF ✅
- B. ifconfig eth0 mac AA:BB:CC:DD:EE:FF
- C. ip link set eth0 address AA:BB:CC:DD:EE:FF
- D. Both A and C ✅

**Q30: In a Linux-based architecture, what does the /mnt directory contain?**
- A. Temporary-mounted filesystems ✅
- B. System mount points
- C. Network shares
- D. Boot files

---

### Cryptography & Authentication

**Q31: A system encrypts data prior to transmitting it over a network, and the system on the other end of the transmission media decrypts it. If the systems are using the symmetric encryption algorithm for encryption and decryption, which of the following statements is true?**
- A. A symmetric encryption algorithm uses the same key to encrypt and decrypt data at both ends of the transmission media ✅
- B. A symmetric encryption algorithm uses different keys at each end
- C. A symmetric encryption algorithm doesn't use keys
- D. A symmetric encryption algorithm only encrypts, not decrypts

**Q32: If a hash begins with $2a$, what hashing algorithm has been used?**
- A. Bcrypt ✅ (also known as Blowfish)
- B. SHA-256
- C. MD5
- D. SHA-1

**Q33: The Diffie-Hellman algorithm is used for _________________.**
- A. Hashing
- B. Digital signatures
- C. Key exchange ✅
- D. Data encryption

**Q34: The cipher in which each letter is replaced by another letter is called __________.**
- A. Transposition
- B. Substitution ✅
- C. Stream cipher
- D. Block cipher

**Q35: Which of the following algorithms could be used to negotiate a shared encryption key?**
- A. AES
- B. RSA
- C. Diffie-Hellman ✅
- D. SHA-256

---

### SSL/TLS

**Q36: The term TLS expands to ________________.**
- A. Transport Level Security
- B. Transport Layer Security ✅
- C. Transmission Layer Security
- D. Transfer Layer Security

**Q37: The term S/MIME refers to ________________.**
- A. Secure/Multipurpose Internet Mail Extensions ✅
- B. Simple/Multipurpose Internet Mail Extensions
- C. Secure/Multipart Internet Mail Extensions
- D. Standard/Multipurpose Internet Mail Extensions

**Q38: Which of the aforementioned SSL/TLS protocols are considered to be unsafe?**
- A. SSLv2 and SSLv3
- B. TLSv1.0 and TLSv1.1
- C. Both A and B ✅
- D. TLSv1.2 and TLSv1.3

**Q39: The application is showing a TLS error message as a result of a website administrator failing to timely renew the TLS certificate. Which of the following statement is correct?**
- A. The communication is no longer encrypted
- B. The communication between the browser and the server is still over TLS ✅
- C. The connection will automatically downgrade to HTTP
- D. The certificate must be renewed before any communication can occur

---

### SSH

**Q40: In the context of the SSH (Secure Shell) public-private key authentication mechanism, which key is uploaded to the server and which key is used by the end-user for authentication?**
- A. The public key is uploaded to the server and the private key is used by the end user for authentication ✅
- B. The private key is uploaded to the server and the public key is used by the end user for authentication
- C. Both keys are uploaded to the server
- D. Both keys are kept by the end user

---

### DNS

**Q41: What ports can be queried to perform a DNS zone transfer?**
- A. 53/TCP ✅
- B. 53/UDP
- C. 853/TCP
- D. 953/TCP

**Q42: What port and protocol are used for a DNS zone transfer?**
- A. 53/TCP ✅
- B. 53/UDP
- C. 853/TCP
- D. 953/UDP

**Q43: Which of the following is a valid DNS record type?**
- A. NAPTR record
- B. SRV record
- C. TXT record
- D. All of the above ✅

**Q44: Which command will perform a DNS zone transfer of the domain "victim.com" from the nameserver at 10.0.0.1?**
- A. dig @10.0.0.1 victim.com axfr ✅
- B. dig victim.com @10.0.0.1 transfer
- C. nslookup -type=axfr victim.com 10.0.0.1
- D. host -t axfr victim.com 10.0.0.1

**Q45: What is the primary security risk associated with a DNS cache poisoning attack?**
- A. The primary risk is that an attacker could manipulate the cache of the DNS server to return a malicious IP address for a legitimate domain name ✅
- B. The DNS server will crash
- C. All DNS queries will be blocked
- D. The DNS server will consume excessive resources

**Q46: You are performing a security audit on a company's infrastructure and have discovered that the domain name system (DNS) server is vulnerable to a DNS cache poisoning attack. What is the primary security risk?**
- A. The primary risk is that an attacker could redirect traffic to a malicious website and steal sensitive information ✅
- B. The DNS server will become unavailable
- C. DNS queries will be significantly slower
- D. The DNS server will require a restart

---

### SMB Protocol

**Q47: Which SMB (Server Message Block) network protocol version introduced support for encrypting SMB traffic?**
- A. SMBv1
- B. SMBv2
- C. SMBv3 ✅
- D. SMBv4

**Q48: Which SMB (Server Message Block) network protocol versions are vulnerable to the EternalBlue (MS17_010) Windows exploit?**
- A. Only SMBv1
- B. Only SMBv2
- C. Only SMBv3
- D. Both SMBv1 and SMBv2 ✅

**Q49: Which version of the SMB protocol introduced data encryption during transit?**
- A. SMBv1
- B. SMBv2
- C. SMBv3 ✅
- D. All versions support encryption

---

### SNMP

**Q50: Which is true for SNMP?**
- A. Default community string for read-only access is public
- B. Default community string for read/write access is private
- C. Both A and B ✅
- D. Neither A nor B

**Q51: You are performing a security audit on a company's network infrastructure and have discovered that the SNMP community string is set to a default value of "public" on several devices. What potential security risks could this pose, and how might you exploit it?**
- A. The potential risk is that an attacker could use the SNMP protocol to gather sensitive information about the devices. You might use a tool like Snmpwalk to query the devices for information ✅
- B. The devices will crash
- C. The network will become unavailable
- D. There is no security risk

**Q52: The Management Information Base (MIB) is a collection of object groups that is managed by which service?**
- A. DNS
- B. SNMP ✅
- C. HTTP
- D. FTP

---

### RPC

**Q53: If you find the 111/TCP port open on a Unix system, what is the next logical step to take?**
- A. Run "rpcinfo -p" to enumerate the RPC services ✅
- B. Run "nmap -sV" to identify the service
- C. Attempt to connect via telnet
- D. Run a vulnerability scan

**Q54: If you find the 111/TCP port open on a Unix system, what is the next logical step to take?**
- A. Run 'rpcinfo -p <hostname>' to enumerate the RPC services ✅
- B. Close the port immediately
- C. Restart the RPC service
- D. Change the port number

---

### Attack Types

**Q55: Which one of the following is not an online attack?**
- A. Brute Force
- B. Rainbow Table Attack ✅
- C. Dictionary Attack
- D. Password Spraying

**Q56: Which of the following is not a DDoS Attack?**
- A. SYN Flood
- B. UDP Flood
- C. ICMP Flood
- D. Brute Force ✅

**Q57: Which of the following attacks are associated with an ICMP protocol?**
- A. Ping Flood
- B. Smurf Attack
- C. Ping of Death
- D. All of the following ✅

**Q58: Which of the following Protocols is not vulnerable to address spoofing attacks if implemented correctly?**
- A. UDP
- B. ICMP
- C. TCP ✅
- D. ARP

---

### Network Segmentation

**Q59: Which of the following techniques can be used to bypass network segmentation during infrastructure penetration testing?**
- A. DNS tunneling
- B. VLAN hopping
- C. Covert channels
- D. All of the above ✅

---

### Authentication & Authorization

**Q60: Which of the following statements regarding Authorisation and Authentication is true?**
- A. Authorisation is the process where requests to access a particular resource is granted or denied. Authentication is providing and validating the identity ✅
- B. Authentication grants access, Authorization validates identity
- C. They are the same thing
- D. Authorization happens before Authentication

---

### Protocol Analysis

**Q61: Which of the following services use TCP protocol?**
- A. DNS
- B. SNMP
- C. HTTP ✅
- D. TFTP

**Q62: Which one of the following services is not an UDP based protocol?**
- A. DNS (queries)
- B. SNMP
- C. TFTP
- D. SSH ✅

**Q63: According to a screenshot showing credentials submitted over HTTPS, which of the following statements is correct?**
- A. The credentials are visible in plain text
- B. The credentials are encrypted in transit
- C. The credentials have been submitted over the HTTPS protocol ✅
- D. The credentials are stored securely

---

### Testing Tools

**Q64: An 'EICAR' file can be used to?**
- A. Test the response of an Anti-virus program ✅
- B. Infect a system with malware
- C. Bypass firewall rules
- D. Exploit a vulnerability

---

## 📊 Answer Key Summary

| Question | Answer | Question | Answer | Question | Answer |
|----------|--------|----------|--------|----------|--------|
| Q1 | A | Q23 | C | Q45 | A |
| Q2 | A | Q24 | D | Q46 | A |
| Q3 | B | Q25 | B | Q47 | C |
| Q4 | A | Q26 | A | Q48 | D |
| Q5 | D | Q27 | C | Q49 | C |
| Q6 | A | Q28 | B | Q50 | C |
| Q7 | C | Q29 | A/D | Q51 | A |
| Q8 | C | Q30 | A | Q52 | B |
| Q9 | B/D | Q31 | A | Q53 | A |
| Q10 | B | Q32 | A | Q54 | A |
| Q11 | A | Q33 | C | Q55 | B |
| Q12 | B | Q34 | B | Q56 | D |
| Q13 | A | Q35 | C | Q57 | D |
| Q14 | B | Q36 | B | Q58 | C |
| Q15 | B | Q37 | A | Q59 | D |
| Q16 | A | Q38 | C | Q60 | A |
| Q17 | B | Q39 | B | Q61 | C |
| Q18 | D | Q40 | A | Q62 | D |
| Q19 | D | Q41 | A | Q63 | C |
| Q20 | A | Q42 | A | Q64 | A |
| Q21 | B | Q43 | D | | |
| Q22 | D | Q44 | A | | |

---

## 🎯 Scoring Guide

- **60-74%**: Pass (38-47 correct out of 64)
- **75-100%**: Pass with Merit (48+ correct out of 64)

If you're consistently scoring 75% or higher on these practice questions, you're ready for the exam!

---

## 📖 Next Steps

- Review incorrect answers and study those topics
- Revisit the [Syllabus](syllabus.md) for weak areas
- Practice hands-on labs for concepts you missed
- Read [My Experience](my-experience.md) for exam tips
- Check [Certification Details](certification.md) for passing criteria
