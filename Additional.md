# Network, Transport, and Application Layers


## Network Layer

### 1. Internet Network Layer

The Internet’s network layer is responsible for managing data forwarding, routing, and handling IP addresses. The main protocols include:

- **IP Protocol**: Defines addressing conventions, datagram format, and packet handling.
- **ICMP (Internet Control Message Protocol)**: Used for error reporting and router signaling.
- **Routing Protocols**: Manage path selection across the network.
  - **Examples**: 
    - **RIP** (Routing Information Protocol): Distance-vector protocol.
    - **OSPF** (Open Shortest Path First): A link-state protocol.
    - **BGP** (Border Gateway Protocol): Manages routes between autonomous systems.

### 2. IP Addressing

- **IP Address**: A 32-bit identifier for devices (hosts or routers) within a network, usually represented in “dotted quad” format (e.g., `223.1.7.4`).
- **Structure**:
  - **Network Part**: High-order bits.
  - **Host Part**: Low-order bits.
- **Interfaces**:
  - Each router has multiple IP addresses, one per network interface.
  - Hosts may have one or multiple IP addresses.

### 3. Routing

Routing determines the optimal path for data to travel from source to destination. Techniques include:

- **Routing Algorithms**:
  - **Static Routing**: Pre-defined routes that change slowly.
  - **Dynamic Routing**: Adapts routes based on network conditions (e.g., congestion).
- **Routing Mechanisms**:
  - **Shortest Path Routing**: Calculates the minimal path between nodes.
  - **Flooding**: Sends packets on all unused links.
  - **Distance Vector Routing**: Uses distance tables to manage the shortest paths.
  - **Link-State Routing**: Each router broadcasts information about directly connected links, enabling optimal path selection.
- **Example**: Finding the shortest path in a network graph based on link cost, where each router has only local knowledge of adjacent nodes.

---

## Transport Layer

The transport layer provides end-to-end data delivery and manages network service quality. It operates on both ends of a connection, enhancing the network layer’s service with reliability and efficiency.

### 1. Functions of the Transport Layer

- **End-to-End Delivery**: Ensures data arrives at its destination.
- **Fragmentation and Multiplexing**: Divides data into smaller units for transmission, managing multiple simultaneous connections.
- **Flow Control**: Adjusts data transmission rates to avoid congestion.
- **Connection Management**: Establishes and terminates data connections.

### 2. Types of Transport Services

- **Connection-Oriented**: Establishes a reliable connection (e.g., TCP).
- **Connectionless**: No fixed connection, suitable for real-time applications (e.g., UDP).
- **Reliability Levels**:
  - **Reliable**: Ensures data integrity.
  - **Unreliable**: Allows faster transmission, with some data loss acceptable.

### 3. Internet Transport Protocols

- **TCP (Transmission Control Protocol)**:
  - **Connection-Oriented**: Establishes a session for reliable communication.
  - **Unicast**: One-to-one communication.
  - **Example**: Web browsing and file downloads, where reliability is crucial.
- **UDP (User Datagram Protocol)**:
  - **Connectionless**: Transmits data without session establishment.
  - **Unicast/Multicast**: One-to-many communication options.
  - **Example**: Video conferencing and online gaming, where speed is prioritized.

---

## Application Layer

The application layer provides network services directly to the end user through various internet applications. It relies on transport layer protocols (TCP and UDP) to deliver data.

### 1. Common Network Applications

- **World Wide Web**: Provides access to web pages using HTTP and HTTPS.
- **Email**: Manages electronic mail with protocols like SMTP (Simple Mail Transfer Protocol), POP3 (Post Office Protocol), and IMAP (Internet Message Access Protocol).
- **File Transfer**: Transfers files over networks, e.g., FTP (File Transfer Protocol) and BitTorrent.
- **Remote Access**:
  - **Remote Desktop**: Microsoft Remote Desktop, VNC, and SSH (Secure Shell).
  - **Remote File Systems**: Accesses files remotely using protocols like NFS (Network File System).

### 2. Client-Server Model

Most internet applications operate on a client-server model where:
  - **Servers**: Always on and often hosted in data centers or the cloud.
  - **Clients**: User devices like PCs or mobile devices.

### 3. Common Application Protocols

- **Web**: HTTP (HyperText Transfer Protocol) and HTTPS.
- **Remote Login**: Telnet and SSH for secure access.
- **Voice/Teleconferencing**: SIP (Session Initiation Protocol) and H.323 for call setup.

### 4. Protocol Format

Protocols often use a client-server model with **command/response** patterns.
  - **Example**: ASCII text commands in email exchange:
    ```
    MAIL From:<sender@example.com>
    RCPT To:<receiver@example.com>
    ```
  - Half-duplex data exchange may be used to alternate transmission and reception, optimizing bandwidth.

---

### Summary
This document covered:
1. **Network Layer**: IP addressing, routing principles, and protocols.
2. **Transport Layer**: End-to-end data delivery and TCP/UDP.
3. **Application Layer**: Internet applications and protocols.

This layered approach ensures efficient, organized data transmission across networks, from physical connections to user-facing applications.