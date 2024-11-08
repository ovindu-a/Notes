# Local Area Networks (LAN)

### Instructor Information
- **Instructor**: Sunimal Rathnayake, CS2033 – Data Communication and Networking
- Based on materials by Prof. Gihan Dias

---

## Lesson Outcomes
- **Objectives**:
  - Explain wired networking concepts, with Ethernet as an example.
  - Identify standards used in Physical and Data Link layers for wired networks.

---

## Types of Networks

Networks vary based on the geographic area they cover and the protocols they use:

- **PAN (Personal Area Network)**: Connects personal devices within a few meters, such as Bluetooth or USB.
- **LAN (Local Area Network)**: Covers a limited area, usually owned by an organization (e.g., office or campus networks).
- **MAN (Metropolitan Area Network)**: Spans up to approximately 30 km, connecting multiple LANs within a city.
- **WAN (Wide Area Network)**: Connects broader geographic regions, such as countries or continents.
- **Interplanetary Networks**: Emerging networks for communication across space.

---

## Network Topologies

The layout or topology defines how devices are connected in a network:

### 1. Bus and Tree Topologies
   - **Bus Topology**: A single communication line connects all stations, with a **tap** for each station.
   - **Tree Topology**: Hierarchical extension of bus topology.
   - **Terminator**: Absorbs signals to remove them from the bus.
   - **Issues**:
     - **Addressing**: Identifying the intended recipient for each communication.
     - **Access Control**: Determining when each station can use the shared medium.
   - **Solution**: Use frames with headers containing destination addresses and control information.

### 2. Ring Topology
   - **Structure**: Stations connected in a closed loop using point-to-point links.
   - **Data Flow**: Unidirectional transmission, where data frames circulate until reaching their destination.
   - **Example**: Each station acts as a repeater, forwarding data along the loop.

### 3. Star Topology
   - **Structure**: Central station (hub or switch) connects all other stations, acting as a relay point.
   - **Communication**: All data passes through the central hub.
   - **Advantages**: Centralized control, easier troubleshooting, and reduced collision risk.

### Topology Choice Factors
   - **Cost**: Setup and maintenance expenses.
   - **Reliability**: Fault tolerance of the network.
   - **Expandability**: Ease of adding more stations.
   - **Performance**: Speed and efficiency in data handling.

---

## Protocols

Protocols define the rules and methods for communication across a network:

- **Multiple Access Links**:
  - **Point-to-Point**: Direct link between two nodes.
  - **Broadcast**: Shared medium (e.g., Ethernet, HFC, 802.11 wireless LAN).

### Multiple Access Protocols
Protocols that govern shared medium access are crucial in avoiding collisions:

1. **Channel Partitioning**: Divides the channel into smaller time slots, frequencies, or codes, each assigned to a node.
   - **TDMA (Time Division Multiple Access)**: Fixed-length time slots for each station.
   - **FDMA (Frequency Division Multiple Access)**: Assigns frequency bands to stations.

2. **Random Access**: Nodes transmit data without pre-coordination, and handle collisions via retransmission.
   - **Examples**: 
     - **ALOHA**: Simple random access.
     - **CSMA (Carrier Sense Multiple Access)**: Checks if the channel is idle before transmitting.
     - **CSMA/CD (Collision Detection)**: Detects and aborts colliding transmissions quickly.

3. **Taking Turns**:
   - **Polling**: A master node invites each node to transmit.
   - **Token Passing**: A token is passed sequentially between nodes, granting transmission permission.

---

## MAC (Medium Access Control) Protocols

MAC protocols fall into three categories:

- **Channel Partitioning**: Time (TDMA), frequency (FDMA), or code division.
- **Random Access**: CSMA/CD (Ethernet) and CSMA/CA (802.11).
- **Taking Turns**: Polling, token ring.

### MAC Addresses
- **Purpose**: Local, unique addresses (48-bit) used to send frames within the same network.
- **Format**: Typically hexadecimal, e.g., `1A-2F-BB-76-09-AD`.

---

## IEEE Standards for Wired Networks

IEEE standards define data rates, topologies, and transmission media for wired networks:

- **802.2**: Logical Link Control (LLC) layer functions.
- **802.3**: Ethernet, including specifications for media and physical layer.
- **802.4**: Token Bus, a bus-based network standard.
- **802.5**: Token Ring, a ring-based network protocol.
- **802.7**: Broadband LAN using coaxial cables.

---

## Ethernet

Ethernet is the most widely used wired LAN technology:

- **History**: Developed by Robert Metcalfe in 1973, originally as part of a PhD thesis.
- **IEEE 802.3**: Standardizes Ethernet specifications.
- **Advantages**:
  - **Cost-effective**: Affordable Network Interface Cards (NICs).
  - **High Speed**: Scales from 10 Mbps to 10 Gbps.
  - **Topology**:
    - **Bus** (popular until the mid-1990s): All nodes in the same collision domain.
    - **Star** (dominant today): Each node connected to a central switch, reducing collisions.

### Ethernet Frame Structure

Frames encapsulate data for transmission with specific headers and footers:

- **Preamble**: 7 bytes `10101010` followed by `10101011` for synchronization.
- **MAC Addresses**: 6-byte source and destination addresses.
- **Type**: Identifies the higher-layer protocol (e.g., IP, Novell IPX).
- **Payload**: Data content, up to 1500 bytes.
- **CRC (Cyclic Redundancy Check)**: Ensures data integrity; dropped if errors are detected.

### Ethernet Characteristics
- **Connectionless**: No handshake between sender and receiver NICs.
- **Unreliable**: Dropped frames aren’t acknowledged; higher layers like TCP handle retransmission if needed.
- **CSMA/CD Protocol**: Manages data transmission and collision detection with a binary backoff strategy.

---

## Summary of MAC Protocols

1. **Channel Partitioning**:
   - **Time Division**: TDMA
   - **Frequency Division**: FDMA

2. **Random Access**:
   - **ALOHA, Slotted ALOHA**
   - **CSMA/CD**: Common in Ethernet
   - **CSMA/CA**: Used in 802.11 wireless networks

3. **Taking Turns**:
   - **Polling**: Master node polling slaves.
   - **Token Passing**: Used in Token Ring and FDDI.

This note covers essential concepts in LAN technologies, topologies, MAC protocols, and Ethernet standards, providing a foundation for understanding wired network structures.