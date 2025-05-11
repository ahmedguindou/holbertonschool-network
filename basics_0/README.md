# 🌐 Networking Fundamentals

This document provides a comprehensive overview of essential networking concepts.

## 🧩 OSI Model

### What it is
The OSI (Open Systems Interconnection) Model is a conceptual framework that standardizes network communications into seven abstraction layers. It allows different network systems to communicate using standard protocols, regardless of their underlying architecture.

### How many layers it has
The OSI Model consists of 7 layers.

### How it is organized
From top to bottom:

1. **Application Layer** 📱 - Interface between the network and user applications (HTTP, FTP, SMTP)
2. **Presentation Layer** 🔄 - Handles data translation, encryption, and compression
3. **Session Layer** 🤝 - Establishes, manages, and terminates connections between applications
4. **Transport Layer** 🚚 - Ensures complete data transfer and quality of service (TCP/UDP)
5. **Network Layer** 🧭 - Determines how data is sent to the receiving device (IP routing)
6. **Data Link Layer** 🔗 - Transfers data between network nodes and handles error detection
7. **Physical Layer** 📡 - Transmits raw bit stream over physical medium (cables, radio waves)

## 🏠 What is a LAN (Local Area Network)

### Typical usage
- Home and office networks
- Connecting computers and devices within limited areas
- Sharing resources (files, printers, internet connection)
- Internal communications within organizations

### Typical geographical size
A LAN typically spans a single building or a group of nearby buildings, such as:
- Home or small office: Few hundred square feet
- School or corporate campus: Few square kilometers

## 🌍 What is a WAN (Wide Area Network)

### Typical usage
- Connecting multiple LANs across large distances
- Corporate networks spanning multiple locations
- Providing infrastructure for internet service providers
- Enabling global communications

### Typical geographical size
WANs cover much larger areas than LANs:
- Can span cities, states, countries, or continents
- Potentially thousands of miles/kilometers
- No theoretical geographical limit

## 🌐 What is the Internet

The Internet is a global system of interconnected computer networks that use the standard Internet Protocol Suite (TCP/IP) to communicate between networks and devices worldwide. It's essentially a "network of networks."

### 🔢 What is an IP address
An IP address is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves two main functions:
- Identifying the host or network interface
- Providing the location of the host in the network

### What are the 2 types of IP address
1. **IPv4 (Internet Protocol version 4)** 4️⃣
   - 32-bit address (e.g., 192.168.1.1)
   - Approximately 4.3 billion unique addresses
   - Written as four decimal numbers separated by periods

2. **IPv6 (Internet Protocol version 6)** 6️⃣
   - 128-bit address (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
   - Vastly larger address space (340 undecillion addresses)
   - Written as eight groups of four hexadecimal digits separated by colons

### 🏠 What is `localhost`
`localhost` refers to the current device you're working on. It's a hostname that means "this computer" and typically resolves to the IP address 127.0.0.1 in IPv4 or ::1 in IPv6. It's used to access network services running on the same machine.

### 🧩 What is a subnet
A subnet is a logical subdivision of an IP network. Subnetting allows network administrators to:
- Divide a large network into smaller, more manageable segments
- Improve network performance by reducing traffic
- Enhance security by isolating network segments
- Use IP addresses more efficiently

### ⏭️ Why IPv6 was created
IPv6 was created primarily because:
- **Address exhaustion**: The ~4.3 billion IPv4 addresses were becoming insufficient for the growing internet
- **Security improvements**: Built-in security features including IPsec
- **Simplified header format**: More efficient routing
- **Elimination of NAT**: Direct end-to-end connectivity without address translation
- **Auto-configuration**: Simplified network management

## 📨 TCP/UDP

### What are the 2 mainly used data transfer protocols for IP
The two main data transfer protocols that operate at the transport layer (layer 4) of the OSI model are:

1. **TCP (Transmission Control Protocol)** 🔒
2. **UDP (User Datagram Protocol)** ⚡

### What is the main difference between TCP and UDP

**TCP:** 🔒
- Connection-oriented protocol
- Reliable data delivery with acknowledgments
- Guaranteed in-order packet delivery
- Flow control and congestion control
- Error detection and recovery
- Used for applications requiring high reliability (web browsing, email, file transfers)

**UDP:** ⚡
- Connectionless protocol
- No delivery guarantees or acknowledgments
- No packet ordering guarantees
- No flow control or congestion control
- Minimal error checking
- Faster and more efficient for applications that can tolerate some data loss (streaming, online gaming, DNS)

### 🚪 What is a port
A port is a 16-bit number (0-65535) that acts as a specific endpoint for communication in a network. Ports allow multiple applications on the same device to use network resources simultaneously by identifying different network services and applications.

### Memorize SSH, HTTP and HTTPS port numbers
- **SSH (Secure Shell)**: Port 22 🔑
- **HTTP (Hypertext Transfer Protocol)**: Port 80 🌐
- **HTTPS (HTTP Secure)**: Port 443 🔒

### 📡 What tool/protocol is often used to check if a device is connected to a network
**ICMP (Internet Control Message Protocol)** is commonly used to check network connectivity, typically through the `ping` utility. Ping sends ICMP echo request packets to the target device and waits for ICMP echo reply packets in return, measuring both connectivity and response time.