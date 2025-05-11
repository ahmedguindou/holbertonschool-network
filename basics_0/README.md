# 🌐 Networking Fundamentals

This document provides a comprehensive overview of essential networking concepts.

## 🧩 OSI Model

### What it is
The OSI (Open Systems Interconnection) Model is a conceptual framework developed by the International Organization for Standardization (ISO) in 1984. It standardizes network communications into seven abstraction layers, creating a universal language for computer networking. This model doesn't represent the actual implementation of networks but serves as a reference tool that allows network designers, operators, and educators to conceptualize how data moves through a network and how different networking technologies interact.

The primary purpose of the OSI model is to facilitate interoperability between diverse communication systems with standard protocols. Before the OSI model, networking was largely proprietary, with equipment from different vendors unable to communicate effectively.

### How many layers it has
The OSI Model consists of 7 distinct layers, each with specific responsibilities and functions. These layers work together in a hierarchical structure where each layer serves the layer above it and is served by the layer below.

### How it is organized
From top to bottom:

1. **Application Layer** 📱 - The layer closest to end users, providing network services directly to applications. It handles:
   - High-level APIs for resource sharing and remote file access
   - Directory services and email
   - Virtual terminals
   - Protocols include: HTTP, FTP, SMTP, DNS, Telnet, SSH, SNMP

2. **Presentation Layer** 🔄 - Prepares data for the application layer, acting as a translator between different data formats:
   - Data compression and decompression
   - Encryption and decryption
   - Character code translation (ASCII, EBCDIC)
   - Implementations include: SSL/TLS, JPEG, GIF, MPEG

3. **Session Layer** 🤝 - Establishes, manages, and terminates connections (sessions) between applications:
   - Controls dialogues between computers
   - Adds checkpoints for long data transfers to enable recovery from network failures
   - Examples: NetBIOS, RPC, SQL

4. **Transport Layer** 🚚 - Ensures complete data transfer by:
   - Segmenting and reassembling data into a data stream
   - Error correction and flow control
   - End-to-end error recovery
   - Key protocols: TCP (connection-oriented) and UDP (connectionless)

5. **Network Layer** 🧭 - Handles routing and forwarding of data packets:
   - Determines optimal path through the network
   - Logical addressing (IP addresses)
   - Traffic control and congestion control
   - Key protocols: IP, ICMP, OSPF, BGP

6. **Data Link Layer** 🔗 - Transfers data between adjacent network nodes:
   - Physical addressing (MAC addresses)
   - Error detection and possible correction
   - Flow control
   - Access to physical media
   - Divided into LLC (Logical Link Control) and MAC (Media Access Control) sublayers
   - Examples: Ethernet, PPP, HDLC, Frame Relay

7. **Physical Layer** 📡 - Transmits raw bit stream over physical medium:
   - Defines electrical, mechanical, and timing specifications
   - Handles physical connections, signaling methods, and transmission rates
   - Examples: RS-232, Ethernet physical layer, USB, Bluetooth physical layer

Data flows down through these layers on the sending device and up through the layers on the receiving device. Each layer adds its own header information (encapsulation) when sending and removes this information (de-encapsulation) when receiving.

## 🏠 What is a LAN (Local Area Network)

### Typical usage
A Local Area Network connects computers and devices in a limited geographical area, providing:

- **Resource sharing**: Centralized access to files, applications, printers, and scanners
- **Collaboration tools**: Shared workspaces, intranet portals, and communication systems
- **Cost efficiency**: Shared internet connections and software licenses
- **Centralized administration**: User account management, security policies, and backups
- **Local hosting**: Internal websites, databases, and applications

Common LAN implementations include:
- **Home networks**: Connecting personal devices like computers, smartphones, smart TVs, and IoT devices
- **Office networks**: Connecting workstations, servers, printers, and VoIP phones
- **School networks**: Computer labs, administrative systems, and educational resources
- **Small business setups**: Point-of-sale systems, inventory management, and customer databases

### Typical geographical size
A LAN typically spans a limited area:
- **Home network**: Single residence (few hundred square feet)
- **Small office**: Single floor or small building (up to several thousand square feet)
- **Corporate environment**: Multi-floor building or campus (up to a few square kilometers)
- **School/University**: Campus buildings (typically under 5-10 km²)

### Technical characteristics
- **Speed**: Typically 1 Gbps to 10 Gbps today
- **Technology**: Usually Ethernet (wired) or Wi-Fi (wireless)
- **Topology**: Star, ring, bus, or mesh configuration
- **Ownership**: Usually owned and managed by a single organization
- **Latency**: Very low (typically under 1ms)

## 🌍 What is a WAN (Wide Area Network)

### Typical usage
A Wide Area Network connects multiple LANs across large geographical distances, enabling:

- **Branch office connectivity**: Linking geographically dispersed locations of an organization
- **Cloud service access**: Providing reliable connections to cloud-based applications and storage
- **Business continuity**: Ensuring access to centralized resources across multiple locations
- **Remote work support**: Enabling VPN access for remote and mobile workers
- **Global operations**: Supporting international business with consistent network services

Common WAN implementations include:
- **Corporate WANs**: Connecting headquarters with branch offices worldwide
- **Government networks**: Linking various agencies and departments across a country
- **Research networks**: Connecting universities and research institutions
- **Backbone networks**: Internet service providers connecting various regions

### Typical geographical size
WANs cover substantially larger areas than LANs:
- **Metropolitan Area Network (MAN)**: City-wide (up to ~100 km)
- **Regional WAN**: State or province (hundreds of kilometers)
- **National WAN**: Country-wide (thousands of kilometers)
- **Global WAN**: Worldwide (tens of thousands of kilometers)

### Technical characteristics
- **Speed**: Typically lower than LANs, ranging from 1.5 Mbps (T1) to 10 Gbps
- **Technology**: Leased lines, MPLS, SD-WAN, satellite links, fiber optic backbones
- **Ownership**: Often uses third-party carrier services (telecommunications companies)
- **Cost**: Significantly higher than LAN infrastructure
- **Latency**: Higher than LANs (tens to hundreds of milliseconds)
- **Reliability considerations**: More points of failure, redundancy often required

## 🌐 What is the Internet

The Internet is a global system of interconnected computer networks using standardized communication protocols, primarily the Internet Protocol Suite (TCP/IP). It's the largest and most well-known WAN, essentially forming a "network of networks."

The Internet evolved from ARPANET, a project funded by the U.S. Department of Defense in the late 1960s. Today it connects billions of devices worldwide and serves as the backbone for the World Wide Web, email, file sharing, streaming media, online gaming, social networking, and countless other services.

Key components of the Internet include:
- **Backbone networks**: High-capacity data routes operated by major internet service providers
- **Internet exchange points (IXPs)**: Facilities where networks interconnect
- **Data centers**: Housing servers that store and process internet content
- **Access networks**: The last-mile connections that bring internet service to homes and businesses

### 🔢 What is an IP address

An IP (Internet Protocol) address is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. IP addresses serve as the foundation of internet connectivity, functioning as both identifiers and locators in the global network.

IP addresses work similarly to postal addresses, but for devices instead of buildings. They enable:
- Unique identification of every device on a network
- Proper routing of data packets across networks to their intended destinations
- Network interface identification
- Location addressing in the network topology

Just as you need someone's correct postal address to send them a letter, computers need the correct IP address to send data to a specific device.

### What are the 2 types of IP address

1. **IPv4 (Internet Protocol version 4)** 4️⃣
   - Developed in the early 1980s as part of the original Internet Protocol specification
   - 32-bit address space represented as four 8-bit octets (e.g., 192.168.1.1)
   - Provides approximately 4.3 billion unique addresses (2³² addresses)
   - Written in dotted-decimal notation with four decimal numbers (0-255) separated by periods
   - Classes: Class A (large networks), Class B (medium networks), Class C (small networks), Class D (multicast), Class E (reserved)
   - Widely deployed but facing exhaustion due to the explosive growth of internet-connected devices

2. **IPv6 (Internet Protocol version 6)** 6️⃣
   - Developed in the mid-1990s to address the anticipated exhaustion of IPv4 addresses
   - 128-bit address space (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
   - Provides approximately 340 undecillion (3.4 × 10³⁸) addresses - enough for trillions of addresses per person
   - Written as eight groups of four hexadecimal digits separated by colons
   - Includes address compression rules to eliminate leading zeros and replace consecutive all-zero groups with a double colon (::)
   - Features improved security, auto-configuration, and more efficient routing

The transition from IPv4 to IPv6 is ongoing, with many networks supporting both protocols simultaneously (dual-stack) to ensure compatibility during the migration period.

### 🏠 What is `localhost`

`localhost` is a hostname that refers to the current device used to access it. It's a loopback mechanism that allows a device to connect to itself rather than to other devices on a network. When a program on your computer connects to "localhost," it's communicating with services running on the same machine, without sending data over external network infrastructure.

Technical details:
- IPv4 address: 127.0.0.1 (though technically any address in the 127.0.0.0/8 range)
- IPv6 address: ::1
- Domain name: localhost

The loopback interface is a virtual network interface implemented entirely in software. When data is sent to localhost, it never leaves the device - the network stack routes the data back to the same machine without transmitting it over any physical network interface.

Common uses for localhost include:
- Testing web servers and applications during development
- Running and accessing local database servers
- Client-server applications running on the same machine
- Inter-process communication
- Network isolation for security purposes

### 🧩 What is a subnet

A subnet (short for subnetwork) is a logical subdivision of an IP network. Subnetting divides a larger network into smaller, more manageable segments, each functioning as its own network.

Subnetting works by borrowing bits from the host portion of an IP address to create a subnet identifier. This process is defined by a subnet mask or CIDR (Classless Inter-Domain Routing) notation, which specifies how many bits are used for the network portion of the address.

For example:
- IP address: 192.168.1.0
- Subnet mask: 255.255.255.0 (or /24 in CIDR notation)
- This means the first 24 bits identify the network/subnet, and the last 8 bits identify hosts

Benefits of subnetting include:

1. **Improved network performance**:
   - Reduces broadcast domain size
   - Decreases network congestion
   - Confines network traffic to relevant segments

2. **Enhanced security**:
   - Creates security boundaries
   - Enables granular access control between subnets
   - Isolates sensitive systems on separate subnets

3. **More efficient address utilization**:
   - Allocates address space according to actual needs
   - Prevents wasting large blocks of addresses on small networks

4. **Simplified management**:
   - Organizes networks by function, department, or location
   - Makes troubleshooting easier
   - Facilitates applying different policies to different network segments

Subnetting is essential for designing efficient, secure, and manageable IP networks of any significant size.

### ⏭️ Why IPv6 was created

IPv6 was developed in the mid-1990s to address several critical limitations of IPv4, with the following being the most significant drivers:

1. **Address exhaustion**: The primary catalyst for IPv6 development was the impending exhaustion of the ~4.3 billion IPv4 addresses. With the rapid growth of:
   - Internet users worldwide (now billions)
   - Mobile devices (multiple per person)
   - IoT devices (projected tens of billions)
   - Cloud computing infrastructure
   The 32-bit address space of IPv4 became insufficient. The Internet Assigned Numbers Authority (IANA) allocated the last blocks of IPv4 addresses to regional internet registries in 2011.

2. **Security improvements**:
   - Built-in IPsec for authentication and encryption (optional in IPv4)
   - Better privacy with temporary address support
   - Simplified security implementation
   - Elimination of address scanning vulnerabilities due to vast address space

3. **Network efficiency**:
   - Streamlined header format (40 bytes fixed vs. variable in IPv4)
   - More efficient routing without fragmentation in routers
   - Elimination of broadcast addresses, replaced by multicast
   - Flow labeling for quality of service

4. **Elimination of NAT (Network Address Translation)**:
   - Direct end-to-end connectivity without address translation
   - Simplifies peer-to-peer applications
   - Restores the original end-to-end principle of the internet
   - Eliminates complications with certain protocols and applications

5. **Auto-configuration capabilities**:
   - Stateless address auto-configuration (SLAAC)
   - Simplified network management
   - Plug-and-play networking
   - Reduced need for DHCP servers

6. **Better multicast and anycast support**:
   - Improved multicast implementation
   - Built-in anycast functionality
   - More efficient group communications

Despite these advantages, IPv6 adoption has been gradual due to:
- Investment in IPv4 infrastructure
- Complexity of transition
- Compatibility concerns
- NAT and other workarounds extending IPv4 lifespan

The internet currently operates with both protocols in a dual-stack configuration in many places, allowing for gradual transition while maintaining compatibility.

## 📨 TCP/UDP

### What are the 2 mainly used data transfer protocols for IP

The two primary data transfer protocols that operate at the transport layer (layer 4) of the OSI model are:

1. **TCP (Transmission Control Protocol)** 🔒
   
   TCP was developed in the 1970s by Vint Cerf and Bob Kahn and is defined in RFC 793. It provides reliable, ordered, and error-checked delivery of data between applications running on hosts communicating over an IP network.

2. **UDP (User Datagram Protocol)** ⚡
   
   UDP, defined in RFC 768, is a simpler, connectionless protocol that operates with minimal overhead but without TCP's reliability mechanisms.

Both protocols function as transport mechanisms for application data, encapsulating it into segments (TCP) or datagrams (UDP) with appropriate headers before passing them to the IP layer for routing across networks. They operate at the transport layer of both the OSI and TCP/IP networking models.

### What is the main difference between TCP and UDP

**TCP (Transmission Control Protocol):** 🔒

- **Connection-oriented**: Establishes a connection before any data transfer through a three-way handshake (SYN, SYN-ACK, ACK)
- **Reliable delivery**: Uses acknowledgments, sequence numbers, and retransmission of lost packets
- **Ordered delivery**: Guarantees that packets arrive in the same order they were sent
- **Flow control**: Uses sliding window mechanism to prevent overwhelming receivers
- **Congestion control**: Dynamically adjusts transmission rates to network conditions
- **Error detection**: Includes checksum and validates data integrity
- **Heavyweight**: Higher overhead due to connection management and reliability features
- **Use cases**: Web browsing (HTTP/HTTPS), email (SMTP/IMAP/POP3), file transfers (FTP, SFTP), remote access (SSH), database connections

Technical aspects:
- Segment structure includes sequence numbers, acknowledgment numbers, window size
- Connection establishment and termination procedures
- Maintains connection state on both ends
- Typical header size: 20-60 bytes

**UDP (User Datagram Protocol):** ⚡

- **Connectionless**: Sends data without establishing a connection first
- **Unreliable delivery**: No acknowledgments, retransmissions, or delivery guarantees
- **No ordering guarantees**: Packets may arrive in any order
- **No flow control**: Does not regulate transmission speed based on receiver capacity
- **No congestion control**: Does not adjust to network congestion
- **Basic error checking**: Simple checksum with no recovery mechanisms
- **Lightweight**: Minimal overhead, resulting in lower latency
- **Use cases**: Live streaming, online gaming, VoIP, DNS lookups, IoT communications, broadcast and multicast applications

Technical aspects:
- Simple datagram structure with minimal header information
- Stateless protocol with no tracking of connections
- Faster transmission due to lack of handshaking and connection management
- Typical header size: 8 bytes

The fundamental tradeoff between TCP and UDP is reliability versus speed. TCP sacrifices some performance for guaranteed delivery and ordering, while UDP maximizes speed and minimizes latency at the expense of reliability. The appropriate choice depends on the specific requirements of the application.

### 🚪 What is a port

A port is a 16-bit number (ranging from 0 to 65535) that acts as a specific endpoint for communication in a network. Ports serve as communication channels, allowing multiple applications on the same device to use network resources simultaneously without interference.

The combination of an IP address and a port number (known as a socket) uniquely identifies a specific process on a specific device in a network. For example, 192.168.1.100:80 refers to the web server (port 80) on the device with IP address 192.168.1.100.

Ports are categorized into three ranges:

1. **Well-known ports (0-1023)**:
   - Reserved for common, standard services
   - Typically require administrative privileges to use
   - Assigned by the Internet Assigned Numbers Authority (IANA)
   - Examples: HTTP (80), HTTPS (443), FTP (21), SSH (22), SMTP (25)

2. **Registered ports (1024-49151)**:
   - Used by specific services but with less stringent requirements
   - Can be registered with IANA but don't require it
   - Examples: MySQL (3306), PostgreSQL (5432), RDP (3389)

3. **Dynamic/Private ports (49152-65535)**:
   - Available for temporary use by client applications
   - Used for outgoing connections and ephemeral purposes
   - Not registered with any authority

The port system enables:
- Multiple services to run on a single server
- Network address translation (NAT) to map external to internal services
- Firewall filtering based on service type
- Load balancing across multiple instances of the same service

When you connect to a website, your computer uses a dynamic port for its end of the connection while connecting to the server's well-known port 80 (HTTP) or 443 (HTTPS).

### Memorize SSH, HTTP and HTTPS port numbers

- **SSH (Secure Shell)**: Port 22 🔑
  - Secure remote administration protocol
  - Provides encrypted command-line access to remote systems
  - Supports secure file transfers with SCP and SFTP
  - Used for secure tunneling and port forwarding
  - Developed as a secure replacement for Telnet (port 23)

- **HTTP (Hypertext Transfer Protocol)**: Port 80 🌐
  - Standard protocol for web browsing
  - Transfers web pages, images, and other web content
  - Unencrypted plaintext protocol
  - Request-response protocol between clients and servers
  - Defined in RFC 2616 and later RFCs

- **HTTPS (HTTP Secure)**: Port 443 🔒
  - Secure version of HTTP using TLS/SSL encryption
  - Protects confidentiality and integrity of data in transit
  - Authenticates the identity of websites via digital certificates
  - Required for secure online transactions and sensitive data
  - Increasingly used as the default for all web traffic

These port numbers are among the most essential to memorize in networking as they represent three of the most commonly used internet protocols. In modern cybersecurity practices, traffic on ports 22 and 443 is typically allowed through firewalls, while restrictions are often placed on unencrypted HTTP traffic on port 80.

### 📡 What tool/protocol is often used to check if a device is connected to a network

**ICMP (Internet Control Message Protocol)** is the standard protocol used to check network connectivity. Unlike TCP and UDP, ICMP operates at the network layer (Layer 3) of the OSI model and is considered part of the Internet Protocol suite.

ICMP was designed for error reporting and diagnostic functions within IP networks. It allows network devices to communicate status and error information to other devices. The protocol is defined in RFC 792 and has been updated in various subsequent RFCs.

The most commonly used implementation of ICMP for connectivity testing is the **ping** utility, which:

- Sends ICMP Echo Request packets to the target device
- Waits for ICMP Echo Reply packets in return
- Measures round-trip time (latency)
- Reports packet loss percentage
- Provides statistics on minimum, maximum, and average response times

Ping syntax example:
```
ping 192.168.1.1
ping www.example.com
```

Other important ICMP-based tools include:

- **Traceroute/tracert**: Maps the path packets take to reach a destination
- **Pathping**: Combines features of ping and traceroute (Windows)
- **MTR (My Traceroute)**: Continuously updated traceroute information (Linux/macOS)

Benefits of ICMP for network diagnostics:
- Simplicity: Easy to use and interpret results
- Low overhead: Minimal impact on network performance
- Universal support: Implemented on virtually all networked devices
- Detailed diagnostics: Provides specific error codes for different network issues

Limitations:
- Often blocked by firewalls and security policies
- Can be rate-limited or deprioritized by network equipment
- Subject to spoofing attacks if not properly secured
- Limited information about higher-layer protocol issues

Network administrators frequently use ICMP-based tools as the first step in diagnosing connectivity problems, before proceeding to more advanced troubleshooting techniques.