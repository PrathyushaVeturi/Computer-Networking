# Introduction to Computer Networks

- It is a collection of interconnected devices that exchange data and share resources.

## Types of Network

To understand the types of Network, think of networking like how devices communicate in different sizes of areas and how they identify each other.

- Smallest → Largest: PAN → LAN → MAN → WAN

### 1. PAN = Personal Area Network

- It is a very small network around a single person.
- Usually within 1–10 meters.
- Example connections:
  - Bluetooth connection between phone and earbuds.
  - Phone hotspot to laptop.

Phone — Bluetooth — Earbuds

Phone - WiFi hotspot -Laptop

### 2. LAN = Local Area Network

- A network covering a small geographic area like (usually managed by one organisation):
  - Home
  - Office
  - School
  - Building
- Examples:
  1. Your home WiFi.

     Router - Laptop / Phone / TV
  2. Office network connecting: (Speed is usually very high)
     - employee computers
     - printers
     - servers
- Example technologies:
  - Ethernet
  - WiFi

### 3. MAN = Metropolitan Area Network

- Network that connects an entire city.
- It connects multiple LANs.
- Example: Internet service providers connecting networks across a city.

Example:

Office LAN —— ISP Network (City) —— College LAN 

- Example organizations:
  - City government networks
  - Cable TV networks

### 4. WAN = Wide Area Network

- A network that spans countries or continents.
- It connects multiple MANs and LANs.
- The Internet is the best example of a WAN.
- Example:

India Network —— Internet (WAN) —— USA Network 

- Other examples:
  - Bank ATM networks
  - Corporate networks across countries

## Network Architecture

- It describes how devices communicate with each other.

### Types

1. Client-Server (Centralized)
2. Peer-to-Peer (Decentralized)

### 1. Client-Server

One powerful computer (server) provides services to many computers (clients).

Advantages:
- centralized control
- easier security
- easier backup

Disadvantages:
- server failure affects everyone

### 2. Peer-to-Peer (P2P)

- All computers are equal. There is no central server.
- Each computer can be both:
  - client
  - server

All nodes communicate directly.

## Understanding MAN, WAN and ISP Connections

- Different LANs cannot communicate directly over long distances.
- Example: Office LAN ↔ ISP Network ↔ College LAN
- So ISPs create city-wide infrastructure using:
  - fiber cables
  - routers
  - switches
  - data centers
- This city-wide network is called MAN (Metropolitan Area Network).
- Examples of ISPs:
  - Airtel
  - Reliance Jio
  - ACT Fibernet

## Netflix Example - Small Networking Notes

- When we open a website like Netflix, the flow would be:
```
Laptop
  │
Home WiFi Router
  │
ISP Network
  │
Internet Backbone
  │
Netflix Server/Data Center
```

### What ISP does
ISP (Internet Service Provider) like:
- Airtel.
- Reliance Jio.

helps carry our request to the destination server using:
- routers.
- switches.
- fiber optic cables.
- undersea cables.

ISP acts like a transport system for internet traffic.

### MAN and WAN in this flow
`Laptop → LAN → MAN → WAN → Netflix Server`

- LAN: Home WiFi/local network.

- MAN: ISP city-wide network infrastructure.

- WAN: Global internet connecting countries/continents.

All three work together.

### Important Understanding
The Netflix server may be:
- in another city.
- another country.
- another continent.

Data travels through physical infrastructure like:
- fiber optic cables.
- routers.
- internet backbone networks.

## Internet Backbone Networks
Internet backbone networks are the main high-speed core networks of the Internet.

They connect:
- countries.
- continents.
- large ISPs.
- major data centers.

Think of them as the main highways of the Internet.

### Who owns backbone networks?
Usually:
- telecom companies.
- large ISPs.
- cloud providers.

Examples:
- Google.
- Amazon.
- Microsoft.

have massive global network infrastructure.

Backbone networks are: **the core infrastructure of the internet**.
- extremely high-speed.
- responsible for long-distance data transfer.

Without backbone networks, global internet communication would not work.

***Internet Backbone*** = The global high-speed infrastructure that carries internet traffic between major networks.

It includes:
```
Backbone Network
├── Land Fiber Networks
├── Undersea Cables
├── Core Routers
├── Internet Exchange Points
└── Data Centers
```

## Protocols (How does the network work?)

```
Device 1 -----(data)----- Device 2
```

- There are some rules to be followed to exchange the data between 2 devices that ensures secure and correct data transmission = "**Protocols**".

### Composition of Protocols
1. Hardware (Physical):
- Cables.
- Connectors.
- NIC.
- Routers.
- Switches.
- Ports.
   - examples:
     - USB (Universal Serial Bus) - Pendrive works with USB protocol.
     - Ethernet.
     - Wifi.

using the Media:
- Copper cable (electrical signals).
- Optical Fibre (light signals).
- Air (radio signals ~ wifi).

2. Software (Logical):
- Formatted.
- Addressed.
- Transmitted.
- Received.

Examples:
- HTTP/S
- TCP/IP
- UDP
- FTP
- telnet
- SMTP
- IP
- TLS
- SSL

## Addressing

### 1. Physical Addressing: 
It refers to identifying a device using its hardware address, called the **MAC Address**.

Every network device has a unique physical identity.
Example:
- Laptop → MAC Address
- Phone  → MAC Address
- Printer → MAC Address

Physical addressing is mainly used for communication inside a LAN.

**Real-world Analogy**:

Think of a person: 
```
Person = Device
Fingerprint = Physical Address (MAC)
```
- A fingerprint uniquely identifies a person.
- Similarly, a MAC Address uniquely identifies a network device.

### 2. Logical Addressing: 

It refers to identifying a device using an **IP Address**.

Unlike MAC addresses, IP addresses can change.

Example:
```
192.168.1.10
10.0.0.5
172.16.1.20
```
Logical addresses are used for communication across networks.

**Real-world Analogy**:
```
Fingerprint = MAC Address
Home Address = IP Address
```
- Your home address can change if you move.
- Similarly, an IP address can change when you connect to a different network.

### Difference between Physical and Logical Addressing:
```
| Physical Addressing | Logical Addressing   |
| ------------------- | -------------------- |
| Uses MAC Address    | Uses IP Address      |
| Hardware based      | Network based        |
| Permanent           | Can change           |
| Used in LAN         | Used across networks |
```

