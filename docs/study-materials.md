# CNSP Study Materials & Preparation Path

The SecOps Group does not provide official training materials or courseware for the CNSP exam. Candidates are expected to prepare through self-study, leveraging existing knowledge, certifications, and practical experience.

## 📚 Recommended Study Resources

### Official Resources
- **The SecOps Group Website**: Check for any official syllabus updates or exam guides
- **CNSP Exam Blueprint**: Review the official exam objectives (if available on their portal)

### Foundational Certifications
If you have these certifications, you already have a strong foundation:
- **CompTIA Security+**: Covers many overlapping security concepts
- **CompTIA Network+**: Excellent for TCP/IP and networking fundamentals
- **Cisco CCNA**: Strong networking foundation, especially for protocols and subnetting

### Books

#### Networking Fundamentals
- **"TCP/IP Illustrated, Volume 1" by W. Richard Stevens**
  - Deep dive into TCP/IP protocols
  - Essential for understanding packet-level behavior

- **"Computer Networking: A Top-Down Approach" by Kurose & Ross**
  - Comprehensive networking fundamentals
  - Great for OSI model and protocol understanding

#### Security Fundamentals
- **"The Web Application Hacker's Handbook" by Dafydd Stuttard**
  - While web-focused, covers many security principles

- **"Hacking: The Art of Exploitation" by Jon Erickson**
  - Hands-on approach to understanding security

- **"Network Security Essentials" by William Stallings**
  - Covers cryptography, authentication, and network security

#### Operating Systems
- **"Windows Internals" by Mark Russinovich**
  - Deep understanding of Windows architecture
  - Useful for AD and Windows security topics

- **"The Linux Command Line" by William Shotts**
  - Free online, excellent for Linux fundamentals

### Online Courses

#### Free Resources
- **Cybrary**: Free courses on networking and security fundamentals
- **Professor Messer (YouTube)**: Free CompTIA Security+ and Network+ videos
- **NetworkChuck (YouTube)**: Engaging networking tutorials
- **HackerSploit (YouTube)**: Security tools and techniques

#### Paid Platforms
- **Udemy**: Look for courses on:
  - Network Security Fundamentals
  - CompTIA Security+ preparation
  - Ethical Hacking basics
  
- **Pluralsight**: Comprehensive networking and security paths

- **INE**: Advanced networking and security training

### Hands-On Practice

#### Virtual Lab Setup
Create a home lab environment:

**Required Software:**
- **VirtualBox** or **VMware Workstation** (free versions available)
- **Kali Linux**: For security tools (Nmap, Wireshark, etc.)
- **Metasploitable 2/3**: Vulnerable VMs for practice
- **Windows Server**: Trial version for AD practice
- **Ubuntu/Debian**: For Linux security practice

**Lab Exercises:**
1. Set up a virtual network with multiple VMs
2. Practice port scanning with Nmap
3. Capture and analyze traffic with Wireshark
4. Configure Active Directory and practice enumeration
5. Practice Linux file permissions (SUID/SGID)
6. Set up and test various network services

#### Online Practice Platforms
- **TryHackMe**: Guided rooms for beginners
  - "Network Security" module
  - "Windows Fundamentals" rooms
  - "Linux Fundamentals" rooms

- **HackTheBox**: More advanced, but great for practice
  - Start with "Starting Point" machines

- **PentesterLab**: Focused exercises on specific topics

### Tools to Master

#### Network Scanning & Analysis
- **Nmap**: Port scanning, service detection
  - Practice different scan types (-sS, -sU, -sV, -O)
  - Understand scan responses
  
- **Wireshark**: Packet analysis
  - Learn to filter traffic
  - Understand TCP handshakes
  - Analyze protocol behavior

#### DNS Tools
- **dig**: DNS queries and zone transfers
  - `dig @nameserver domain.com axfr`
  - Query different record types
  
- **nslookup**: Alternative DNS query tool

#### Windows Tools
- **net commands**: User and group management
- **klist**: Kerberos ticket verification
- **PowerShell**: Modern Windows administration

#### Linux Tools
- **ifconfig/ip**: Network configuration
- **chmod/chown**: File permissions
- **rpcinfo**: RPC service enumeration

#### SNMP Tools
- **snmpwalk**: SNMP enumeration
- **onesixtyone**: SNMP community string scanner

---

## 🗓️ Suggested Study Plan

### Week 1-2: Networking Fundamentals
- [ ] Review OSI model and TCP/IP stack
- [ ] Practice subnetting and CIDR notation
- [ ] Memorize common ports and protocols
- [ ] Understand TCP vs. UDP
- [ ] Practice with Nmap and Wireshark

### Week 3: Windows Security
- [ ] Set up Windows Server VM
- [ ] Practice Active Directory basics
- [ ] Learn Windows file system and registry
- [ ] Practice `net` commands
- [ ] Study Kerberos authentication

### Week 4: Linux Security
- [ ] Set up Linux VM
- [ ] Practice file permissions (SUID/SGID)
- [ ] Learn important file system paths
- [ ] Practice basic Linux commands
- [ ] Understand daemon processes

### Week 5: Cryptography & Authentication
- [ ] Study symmetric vs. asymmetric encryption
- [ ] Learn hashing algorithms and identifiers
- [ ] Understand SSL/TLS versions
- [ ] Study key exchange mechanisms
- [ ] Practice SSH key authentication

### Week 6: Network Services & Attacks
- [ ] Study common network services
- [ ] Learn SNMP security
- [ ] Understand SMB versions and vulnerabilities
- [ ] Study attack types (DDoS, DNS poisoning, etc.)
- [ ] Practice service enumeration

### Week 7: Review & Practice
- [ ] Take practice questions
- [ ] Review weak areas
- [ ] Do hands-on labs
- [ ] Simulate exam conditions
- [ ] Final review of all topics

---

## 📝 Study Tips

### Active Learning
- **Don't just read**: Practice every concept in a lab
- **Take notes**: Write down key facts and commands
- **Teach others**: Explaining concepts reinforces learning
- **Create flashcards**: For ports, commands, and key facts

### Focus Areas
Based on the exam questions, prioritize:
1. **Port numbers and protocols**: Know them cold
2. **Scan responses**: Understand all scenarios (firewall/no firewall, TCP/UDP)
3. **Windows commands**: Practice `net` commands extensively
4. **File permissions**: Understand SUID/SGID visually
5. **Cryptography basics**: Know algorithm names and uses

### Common Pitfalls to Avoid
- ❌ Memorizing without understanding
- ❌ Skipping hands-on practice
- ❌ Ignoring scenario-based questions
- ❌ Not timing yourself during practice
- ❌ Studying only theory without practical application

### Exam Day Preparation
- [ ] Test your equipment (camera, microphone) beforehand
- [ ] Ensure stable internet connection
- [ ] Clear your desk and testing area
- [ ] Have ID ready for verification
- [ ] Get good sleep the night before
- [ ] Arrive early to handle any technical issues

---

## 🎯 Knowledge Check

Before scheduling your exam, ensure you can answer:

- What is the response from an open TCP port?
- How many usable TCP/UDP ports are there?
- Where are Linux password hashes stored?
- What is the RID of the Windows Administrator account?
- Which SMB version introduced encryption?
- What port is used for DNS zone transfers?
- What does a hash beginning with $2a$ indicate?
- Which SSL/TLS versions are unsafe?
- What is the difference between SUID and SGID?
- How does Diffie-Hellman work?

If you can confidently answer these and similar questions, you're ready!

---

## 📖 Next Steps

- Review [Practice Questions](practice-questions.md) to test your knowledge
- Read [My Experience](my-experience.md) for exam tips and insights
- Check [Certification Details](certification.md) for passing criteria
- Schedule your exam when you consistently score 75%+ on practice questions
