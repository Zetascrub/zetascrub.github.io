# Methodologies

## Engagements

## Prerequisite

- [ ] Confirm scope
- [ ] If scope is external, check a sample size (if not all) of what's in scope (URL/IP) to ensure they belong to the client
- [ ] Confirm testing hours
- [ ] Confirm what's out of scope (typically DOS)
- [ ] Update tools & confirm your VM boots

## Starting engagement

- [ ] Send "Start" email, designating the time the automated scans will start.

## During engagement

#### Critical Vulnerability

If a critical vulnerability has been discovered, pause the assessment and contact the escalation point to inform.
**NOTE: Don't email the client the details of the vulnerability unless explicitly asked to do so by the client.**

## End of engagement

- [ ] Ensure all required evidence has been collected
- [ ] Confirm all scope has been tested
- [ ] Send "End" email, giving the client achknowledgement that the testing is over, should they wish to remove whitelists

## Reporting

- [ ] Replace {{ client }}
- [ ] Replace {{ Test Type }}
- [ ] Replace \[Summary of Test Target\] in section 2.1 - Scope of Testing
- [ ] Summary of Findings
- [ ] Information Provided
- [ ] Limitations & Constraints
- [ ] Check Dates
- [ ] Priority Recommendations
- [ ] Confirm white label (Softcat / Evalian) and replace if required
- [ ] Ensure findings are in order of descending CVSSv3 values
- [ ] Ensure finding refences are placed within section 3.2 - Summary of Vulnerabilities
- [ ] Updated table of contents
- [ ] Save document within client folder
    **Example:** /Acme Inc/Penetration Testing/20211020\_ACMPEN01\_External Infrastructure\_Report\_v0.1.doc

## Web Applications

### Information Gathering

- [ ] Conduct search engine discovery reconnassance for information leakage
- [ ] Fingerprint web server
- [ ] Review webserver metafiles for information leakage
- [ ] Enumerate application on web server
- [ ] Review webpage comments and metadata for information leakage
- [ ] Identify application entry points
- [ ] Map execution paths through application
- [ ] Fingerprint web application Framework
- [ ] Fingerprint web application
- [ ] Map application architecture

### Configuration and Deployment management Testing

- [ ] Test network infrastructure configuration
- [ ] Test application platform configuration
- [ ] Test file extensions handling for sensitive information
- [ ] Review old backup and unreferenced files for sensitive information
- [ ] Enumerate infrastructure and application admin interfaces
- [ ] Test HTTP methods
- [ ] Test HTTP strict transport security
- [ ] Test RIA Cross domain policiy
- [ ] Test file permissions
- [ ] Test for subdomain takeover
- [ ] Test cloud storage

### Identity Management Testing

- [ ] Test role definitions
- [ ] Test user registration process
- [ ] Test account provisioning process
- [ ] Testing for account enumeration and guessable user account
- [ ] Testing for weak or unenforced username policy

### Autentication Testing

- [ ] Testing for credentials transported over an encrypted channel
- [ ] Testing for default credentials
- [ ] Testing for weak lockout mechanism
- [ ] Testingfor bypassing authentication schema
- [ ] Testing for vulnerable remember password
- [ ] Testing for browswer cache weaknesses
- [ ] Testing for weak password policy
- [ ] Testing for weak security question answer
- [ ] Testing for weak password change or reset functionalities
- [ ] Testing for weaker authentication in alternative channel

### Authorisation Testing

- [ ] Testing directory traversal file include
- [ ] Testing for bypassing authorisation schema
- [ ] Testing for privilege escalation
- [ ] Testing for insecure direct object references

### Session Management Testing

- [ ] Testing for session management schema
- [ ] Testing for cookies attributes
- [ ] Testing for Session fixation
- [ ] Testing for exposed session variables
- [ ] Testing for cross site request forgery
- [ ] Testing for logout functionality
- [ ] Testing session timeout
- [ ] Testing for session puzzling

### Input Validation Testing

- [ ] Testing for reflected cross site scripting
- [ ] Testing for stored cross site scripting
- [ ] Testing for HTTP verb tampering
- [ ] Testing for HTTP parameter polution
- [ ] Testing for SQL injection
- [ ] Testing for LDAP injection
- [ ] Testing for XML injection
- [ ] Testing for for SSI Injection
- [ ] Testing for XPath injection
- [ ] Testing for IMAP SMTP injection
- [ ] Testing for code injection
- [ ] Testing for command injection
- [ ] Testing for buffer overflow
- [ ] Testing for incubated vulnerability
- [ ] Testing for HTTP splitting smuggling
- [ ] Testing for HTTP incoming requests
- [ ] Testing for host header injection
- [ ] Testing for server side template injection

### Testing for Error Handling

- [ ] Testing for error codes
- [ ] Testing for stack traces

### Testing for Weak Cryptography

- [ ] Testing for weak SSL or TLS cipher or insufficient transport layer protection
- [ ] Testing for paddle oracle
- [ ] Testing for sensitive information sent via unencrypted channels
- [ ] Testing for weak encryption

### Business Logic Testing

- [ ] Test business logic data validation
- [ ] Test ability to forge requests
- [ ] Test integrity checks
- [ ] Test for process timing
- [ ] Test number of times a function can be used limits
- [ ] Testing for the circumventation of workflows
- [ ] Test defences against application misuse
- [ ] Test upload of unexpected filetypes
- [ ] Test upload of malicious files

### Client Side Testing

- [ ] Testing for DOM-based cross site scripting
- [ ] Testing for JavaScript execution
- [ ] Testing for HTML injection
- [ ] Testing for client side URL redirect
- [ ] Testing for CSS injection
- [ ] Testing for client side resource manipulation
- [ ] Testing cross origin resource sharing
- [ ] Testing for cross site flashing
- [ ] Testing for clickjacking
- [ ] Testing websockets
- [ ] Testing web messaging
- [ ] Testing browser storage
- [ ] Testing for cross site script inclusion

## Internal (Needs reviewing)

### Recon

- [ ] Map the Internal Network
- [ ] Scan the Network for Live Hosts
- [ ] Port-scan individual machines
- [ ] Utilise Responder
- [ ] Sniff the network using Wireshark
- [ ] Sniff POP3/FTP/Telnet Passwords
- [ ] Capture POP3 Traffic
- [ ] Capture SMTP Traffic
- [ ] Capture IMAP E-mail traffic
- [ ] Capture the communications between FTP client and FTP Server
- [ ] Capture HTTP Traffic
- [ ] Capture RDP Traffic
- [ ] Capture VoIP Traffic
- [ ]  Enumerate users/identify domains on the network

### Gain Access

- [ ]  Try to gain access using known vulnerabilities
    
- [ ]  Attempt to establish null sessions
    
- [ ]  Try logging in to a console machine
    
- [ ]  Attempt Replay Attacks
    
- [ ]  Attempt ARP Poisoning
    
- [ ]  Attempt MAC Flooding
    
- [ ]  Conduct Man-In-The-Middle Attacks
    
- [ ]  Attempt DNS Poisoning
    
- [ ]  Boot the PC Using an Alternate OS and Steal the SAM File
    
- [ ]  Bypass the OS to Obtain Information
    
- [ ]  Attempt to plant a software keylogger to steal passwords.
    
- [ ]  Attempt to plant a hardware keylogger to steal passwords.
    
- [ ]  Attempt to plant spyware on the target machine
    
- [ ]  Attempt to plant a Trojan on the target machine
    
- [ ]  Attempt to to bypass antivirus software installed on the target machine
    

~~Attempt to send a virus using the target machine.~~
~~Attempt to to plant rootkits on the target machine~~
~~Hide sensitive data on target machine~~
~~Hide hacking tools and other data on target machines~~
~~Use various steganography techniques to hide files on target machines.~~

- [ ]  Escalate user privileges
- [ ]  Run Wireshark with the filter -ip.src == ip_address
- [ ]  Run Wireshark with the filter -ip.dst == ip_address
- [ ]  Run Wireshark with the filter -tcp.dstport == port_no
- [ ]  Run Wireshark with the filter -ip.addr == ip_address
- [ ]  Spoof the MAC Address
- [ ]  Attempt Session Hijacking on telnet traffic.
- [ ]  Attempt Session Hijacking on FTP traffic.
- [ ]  Attempt Session Hijacking on HTTP traffic.

## External (Need reviewing)

- [ ]  Inventory Company’s External Infrastructure
- [ ]  Create Topological Map of Network
- [ ]  Identify IP Addresses of the Target
- [ ]  Locate the traffic routes that go the servers
- [ ]  Trace the TCP traffic Path to the destination
- [ ]  Trace the UDP traffic Path to the destination
- [ ]  Identify the physical location of the target servers
- [ ]  Examine the use of IPv6 at the remote location
- [ ]  Look up the domain registry for IP information
- [ ]  Find IP lock information about the target
- [ ]  List Open Ports
- [ ]  List Close Ports
- [ ]  List Suspicious Ports that may be stealth ports
- [ ]  Port scan every port on the targets network
- [ ]  Use SYN scan on the target and analyze the response.
- [ ]  Use connect scan on the target and analyze the response.
- [ ]  Use Xmas scan on the target and analyze the response.
- [ ]  Use FIN scan on the target and analyze the response.
- [ ]  Use null scan on the target and analyze the response.
- [ ]  Examine TCP sequence number prediction
- [ ]  Examine the use of standard and nonstandard protocol.
- [ ]  Examine IP ID sequence number prediction
- [ ]  Examine the system uptime of the target
- [ ]  Examine the operating system used by different targets
- [ ]  Examine the patches applied to the operating system
- [ ]  Locate the DNS record of the domain and attempt DNS Hijacking
- [ ]  List programming languages and application software used to create various programs on the target server
- [ ]  Look for errors and custom web pages
- [ ]  Guess different subdomain names and analyze different responses
- [ ]  Hijack sessions
- [ ]  Examine cookies generated by the server
- [ ]  Examine the Access Control used by the Web Server
- [ ]  Brute-force URL injection and session tokens
- [ ]  Check for directory consistency and page-naming syntax of the Web pages.
- [ ]  Look for sensitive information in the Web page source code.
- [ ]  Try buffer overflow attempts in input fields.
- [ ]  Look for invalid ranges in input fields.
- [ ]  Attempt escape-character injection
- [ ]  Try Cross-Site Scripting techniques.
- [ ]  Record and replay the traffic to the target Web Server and note the response
- [ ]  Try various SQL-injection techniques
- [ ]  Examine hidden fields
- [ ]  Examine Server-Side Includes (SSI)
- [ ]  Examine e-commerce and payment gateways handled by the Web Server
- [ ]  Examine welcome, error, and debug messages.
- [ ]  Probe the server through SMTP mail bouncing.
- [ ]  Grab the banners of HTTP Server
- [ ]  Grab the banners of SMTP Server
- [ ]  Grab the banners of POP3 Servers.
- [ ]  Grab the banners of FTP Servers.
- [ ]  Identify the Web Extensions used on the server
- [ ]  Try to use an HTTPS tunnel to encapsulate traffic.
- [ ]  OS Fingerprint Target Servers
- [ ]  Check for ICMP Responses (Type 3 Port Unreachable)
- [ ]  Check for ICMP Responses (Type 8 Echo Request)
- [ ]  Check for ICMP Responses (Type 13 Time-Stamp Request)
- [ ]  Check for ICMP Responses (Type 15 Information Request)
- [ ]  Check for ICMP Responses (Type 17 Subnet Address Mask Request)
- [ ]  Check for ICMP Responses from broadcast address.
- [ ]  Port Scan DNS Server (TCP/UDP 53)
- [ ]  Port Scan TFTP Servers (Port 69)
- [ ]  Test for NTP Ports (Port 123)
- [ ]  Test for SNMP Ports (Ports 161,162)
- [ ]  Test for Telnet Ports (Port 23)
- [ ]  Test for LDAP Ports (Port 389)
- [ ]  Test for NetBIOS Ports (Port 135–139 and 445)
- [ ]  Test for SQL Server Ports (Port 1433 and 1434)
- [ ]  Test for Citrix Ports (Port 1495)
- [ ]  Test for Oracle Ports (Port 1521)
- [ ]  Test for NFS Ports (Port 2049)
- [ ]  Test for RDP Ports (Port 3389)
- [ ]  Test for Sybase Ports (Port 5000)
- [ ]  Test for SIP Ports (Port 5060)
- [ ]  Test for VNC Ports (Port 5800 and 900)
- [ ]  Test for X11 Ports (Port 6000)
- [ ]  Test for FTP Ports (Port 20)
- [ ]  Test for Web Server Ports (Port 80)
- [ ]  Test for SSL Server Ports (Port 443)
- [ ]  Test for Kerberos and AD Ports (Port TCP/UDP 88)
- [ ]  Test for SSH Servers Ports (Port 22)

## Firewall (Needs reviewing)

- [ ]  Locate the Firewall
- [ ]  Conduct a traceroute to identify the network range
- [ ]  Port Scan the firewall
- [ ]  Grab the Banner
- [ ]  Create Custom packets and look for firewall responses
- [ ]  Test Access Control Enumeration
- [ ]  Test to identify Firewall architecture
- [ ]  Test Firewall Policy
- [ ]  Test Firewall Using the Firewalk Tool
- [ ]  Test for Port Redirection
- [ ]  Test the firewall from both sides
- [ ]  Test Covert Channels
- [ ]  Perform a Covert Firewall Test From the Outside
- [ ]  Test HTTP Tunneling
- [ ]  Test Firewall-specific vulnerabilities
- [ ]  Document Everything

## Social Enginering (Needs reviewing)

### Resources

- https://osintframework.com/

## Red Teaming