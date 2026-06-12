# Layers of Networking

## OSI Model

The OSI Model (Open Systems Interconnection Model) is one of the most important concepts in networking because it explains how data travels from one device to another.

Think of it as a 7-layer communication process.

### Why do we need the OSI Model?
Suppose you send a message:

`Your Laptop  →  Internet  →  Netflix Server`

A lot happens behind the scenes:
- Data is created
- Data is formatted
- Data is encrypted
- Data is assigned IP addresses
- Data is assigned MAC addresses
- Data is converted to signals
- Data travels through cables/WiFi

OSI divides all these tasks into 7 layers.

**OSI Model Overview**:
```
7.Application
6.Presentation
5.Session
4.Transport
3.Network
2.Data Link
1.Physical
```

Memory Trick:
```
All
People
Seem
To
Need
Data
Processing
```

## Layers
### 7. Application Layer:
Provides network services directly to applications used by users.

Examples:
- Web browsing
- Email
- File transfer

Protocols:
- HTTP
- HTTPS
- FTP
- SMTP
- DNS

Example:
```
Chrome Browser
      │
Application Layer
```
When you enter:
`www.netflix.com`
the request starts here.

### 6. Presentation Layer:
Responsible for:
- Data formatting
- Encryption
- Decryption
- Compression

Think of it as a translator.

Example:
```
Application Data
      │
Presentation Layer
      │
Formatted Data
```
Encryption Example:

When using HTTPS:
```
Original Data
      │
Encrypted
      │
Internet
```
Protocols/Technologies:
- SSL/TLS
- JPEG
- PNG
- ASCII
- UTF-8

### 5. Session Layer:
Creates and manages communication sessions.

Responsibilities:
- Establish session
- Maintain session
- Terminate session

Example:
```
Laptop
   │
Session Created
   │
Netflix Server
```
While watching a movie, the session remains active.

### 4. Transport Layer:
Ensures reliable delivery of data.

Protocols:
- TCP
- UDP

**TCP (Reliable)**:

Features:
- Error checking
- Retransmission
- Ordered delivery

Example:
- Websites
- Banking
- Emails

TCP ensures no data is lost.

**UDP (Fast)**:

Features:
- Faster
- No guarantee of delivery

Example:
- Video calls
- Gaming
- Streaming
- Port Numbers

Transport Layer uses ports.

Examples:
```
80   → HTTP
443  → HTTPS
22   → SSH
```

### 3. Network Layer:
Handles logical addressing and routing.

Uses:
- IP Addresses
- Routers

Protocols:
- IPv4
- IPv6
- ICMP

Example
```
Laptop IP:
192.168.1.10

Netflix Server IP:
52.x.x.x
```
Router uses these IPs to find the path.

### 2. Data Link Layer:
Handles communication within a local network.

Uses:
- MAC Addresses
- Switches

Example
```
Laptop MAC
      │
Switch
      │
Router MAC
```
Frame contains:
- Source MAC
- Destination MAC

This is where MAC addressing works.

### 1. Physical Layer:
Transfers raw bits.

Responsible for:
- Cables
- Fiber optics
- WiFi signals
- Electrical signals

Example:
`0 1 0 1 1 0 0 1`

Actual transmission happens here.

## Data Encapsulation
As data moves down the OSI model, each layer adds information.

Example:
```
Application Data
        │
Transport Header
        │
Network Header
        │
Data Link Header
        │
Physical Signals
```
This process is called ***Encapsulation***.

Data Unit Names
```
----------------------------
| Layer        | Data Unit |
| ------------ | --------- |
| Application  | Data      |
| Presentation | Data      |
| Session      | Data      |
| Transport    | Segment   |
| Network      | Packet    |
| Data Link    | Frame     |
| Physical     | Bits      |
----------------------------
```
## Netflix Example Using OSI
When you open Netflix:
```
Application Layer
↓
HTTPS Request
↓
Transport Layer
(TCP Port 443)
↓
Network Layer
(IP Address)
↓
Data Link Layer
(MAC Address)
↓
Physical Layer
(WiFi/Fiber Signals)
↓
Internet
↓
Netflix Server
```

## Quick Touch:
```
------------------------------------------------------------------
| Layer | Name         | Main Function          | Examples       |
| ----- | ------------ | ---------------------- | -------------- |
| 7     | Application  | User services          | HTTP, DNS      |
| 6     | Presentation | Encryption, Formatting | TLS, JPEG      |
| 5     | Session      | Session management     | Login sessions |
| 4     | Transport    | Reliability, Ports     | TCP, UDP       |
| 3     | Network      | Routing, IP            | IPv4, IPv6     |
| 2     | Data Link    | MAC communication      | MAC, Switch    |
| 1     | Physical     | Signal transmission    | Fiber, WiFi    |
------------------------------------------------------------------
```

