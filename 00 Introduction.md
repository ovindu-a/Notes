# Introduction

### 1. Communication and Networks

- **Communication**: The process of sending information from one place to another, which may be over a physical connection or through various mediums (like radio waves or fiber optics).
  - **Types of Communication**:
    - **Video**: Live or recorded visual data, such as video conferencing.
    - **Text**: Communication using written characters, such as emails or text messages.
    - **Voice**: Audio communication, including phone calls or voice messages.
    - **Data**: Information transferred electronically, such as file downloads.
    - **Multimedia**: A combination of video, text, voice, and data, like in streaming services.
  - **Information Flow**:
    - **One-way**: Data flows in one direction only, e.g., a broadcast radio.
    - **Interactive (Non-real-time)**: Communication happens in both directions, but with delays, like email exchanges.
    - **Interactive (Real-time)**: Instant, two-way communication, e.g., video calls.
  - **Number of Parties**:
    - **Two-party**: Communication between two entities, e.g., a phone call.
    - **Multi-party**: Communication involving multiple parties, such as video conferences.

- **Network**: A system that connects devices to facilitate communication.
  - **Examples of Networks**:
    - **PSTN** (Public Switched Telephone Network): Traditional landline phone network.
    - **LAN** (Local Area Network): Network within a limited area like a building.
    - **Internet**: A global network connecting millions of devices.
    - **Vehicular Networks**: Networks connecting vehicles for data exchange, such as in smart traffic systems.

- **Components of a Network**:
  - **Terminals**: Devices that serve as network access points, like computers or smartphones.
  - **Switching Equipment**: Directs traffic within the network, like routers and switches.
  - **Transmission Media**: Carries data across the network, such as copper cables, fiber optics, or wireless signals.

### 2. Layered Architecture

- **Modularization, Layering, Standardization**: These design principles allow different systems to communicate regardless of hardware, software, or geographical differences.
- **OSI Model (Open Systems Interconnection)**: A seven-layer model that provides a standard for communication between different systems.

---

### 3. OSI Model Layers

The OSI (Open Systems Interconnection) model organizes communication into seven distinct layers, each responsible for different aspects of data transmission. Each layer performs a specific role and communicates with adjacent layers. Here’s a breakdown with examples:

#### **1. Physical Layer**
   - **Purpose**: Responsible for the transmission and reception of raw binary data over a physical medium.
   - **Functions**:
     - **Encoding and Signaling**: Converts data into signals suitable for the medium (e.g., electrical pulses for copper wires).
     - **Transmission and Reception**: Moves data physically across cables or airwaves.
     - **Topology and Design**: Dictates the network’s physical layout, like star or mesh topology.
   - **Examples**: 
     - **Ethernet cables** transmit data as electrical signals.
     - **Wi-Fi** uses radio waves for wireless data transmission.

#### **2. Data Link Layer**
   - **Purpose**: Ensures error-free transmission between two directly connected nodes by detecting and correcting errors.
   - **Functions**:
     - **Framing**: Encapsulates raw data into frames for error-checking and delivery.
     - **Error Detection and Handling**: Identifies and corrects errors in data transmission.
     - **Flow Control**: Manages the data flow to prevent overload.
     - **Addressing**: Directs data to specific devices using **MAC (Media Access Control)** addresses.
   - **Examples**:
     - **Wi-Fi** and **Ethernet protocols** work here, using MAC addresses to identify devices in a local network.

#### **3. Network Layer**
   - **Purpose**: Handles packet delivery across the network, finding the best route from the source to the destination.
   - **Functions**:
     - **Logical Addressing**: Uses IP (Internet Protocol) addresses to identify devices.
     - **Routing**: Determines the optimal path to send data packets.
     - **Datagram Encapsulation**: Packages data with routing information.
     - **Congestion Control and Quality of Service (QoS)**: Manages network traffic to optimize performance.
   - **Examples**:
     - **IP** (Internet Protocol) works at this layer, such as when data is routed between devices across the internet.
     - When sending an email, IP addresses route the data from your computer to the server and to the recipient.

#### **4. Transport Layer**
   - **Purpose**: Manages end-to-end communication and data integrity between host devices.
   - **Functions**:
     - **Connection Establishment, Management, and Termination**: Initiates and maintains communication sessions.
     - **Multiplexing/Demultiplexing**: Manages multiple applications using the network simultaneously.
     - **Error Detection and Correction**: Ensures data arrives without errors.
     - **Flow Control and QoS**: Controls the data rate and manages performance requirements.
   - **Examples**:
     - **TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)** operate here.
     - For video streaming, **TCP** ensures data packets arrive in the correct order, while **UDP** allows some loss of data to prioritize speed over accuracy.

#### **5. Session Layer**
   - **Purpose**: Manages and controls dialogues (sessions) between two communicating applications.
   - **Functions**:
     - **Dialog Control**: Determines communication modes like full duplex (both directions simultaneously) or half duplex (one direction at a time).
     - **Token Management**: Prevents simultaneous transmission conflicts.
     - **Synchronization**: Manages checkpoints and recovery, allowing resumed transmission if interrupted.
   - **Examples**:
     - **SSH (Secure Shell)**: When accessing a remote server, the session layer manages the session, maintaining the connection until logout.

#### **6. Presentation Layer**
   - **Purpose**: Formats and processes data for application layer access, including data translation, compression, and encryption.
   - **Functions**:
     - **Translation**: Converts data formats, such as ASCII to Unicode.
     - **Compression**: Reduces data size for faster transmission.
     - **Encryption**: Secures data during transmission.
   - **Examples**:
     - **SSL/TLS**: Encrypts data for secure HTTP (HTTPS), ensuring that data like passwords are safe during transmission over the web.

#### **7. Application Layer**
   - **Purpose**: Interfaces with network-based applications, providing services directly to the user.
   - **Functions**:
     - Supports applications like file transfer, email, and web browsing.
   - **Examples**:
     - **HTTP (Hypertext Transfer Protocol)** and **HTTPS** allow web browsing.
     - **SMTP (Simple Mail Transfer Protocol)** manages email transmission.

---

### 4. Scope of CS2033
- **In-depth Study**: Physical Layer
- **Touchpoints**: Data Link Layer
- **Brief Introduction**: Network Layer and Application Layer

---
