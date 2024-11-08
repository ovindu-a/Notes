# Network Applications: Storage, DNS, and Peer-to-Peer (P2P)

### Author: Sunimal Rathnayake, Slides by Prof. Gihan Dias

---

## 1. File Storage

### Overview
- **Storage Location**: Files are stored on a network server.
- **Access**: Accessed by clients, often through user interfaces like Windows Explorer.
- **Methods**: Files can be accessed via web browsers or dedicated client applications.

### File Transfer Protocol (FTP)
- **Purpose**: Original protocol for transferring files to/from clients and servers.
- **Date**: Defined in 1980.
- **Connections**:
  - **Control Connection**: TCP port 21, handles commands.
  - **Data Connection**: TCP port 20, handles data transfer.
- **Authentication**: Requires username and password for access.

### Common FTP Commands
- `USER <username>`: Identify user.
- `PASS <password>`: Authenticate user.
- `LIST`: List files in the current directory.
- `RETR <filename>`: Retrieve a file.
- `STOR <filename>`: Upload a file.

### Secure File Transfer Protocol (SFTP)
- **Description**: A secure version of FTP using Transport Layer Security (TLS).
- **Interface**: Often used with GUI clients.

---

## 2. Network File Systems (NFS)
- **Purpose**: Provides file access over a network (also called Network Attached Storage, NAS).
- **Operating Systems**:
  - **Unix**: Uses Network File System (NFS).
  - **Windows**: Uses SMB (Server Message Block) and CIFS (Common Internet File System).
- **Function**: Allows a client to mount a server’s file system as a drive, enabling file operations like open, read, and write.

---

## 3. Storage-Area Networks (SAN)
- **Purpose**: Specialized storage devices with block-level access.
- **Features**:
  - High performance.
  - Storage shared among servers (not clients).
  - Managed via specialized tools.

### Internet Storage
- **Example Services**: Dropbox, Google Drive.
- **Purpose**: Provides storage space, backup, and remote access.
- **Protocols**: Often uses WebDAV, SMB.

---

## 4. Domain Name System (DNS)

### Introduction
- **IP Addresses**: Hosts on the Internet are identified by numeric IP addresses (e.g., 192.248.8.100).
- **Hostnames**: Alphanumeric hostnames are used for ease of use.
- **DNS Purpose**: Maps human-friendly hostnames to IP addresses.
- **Origins**: Originally managed by a centralized `/etc/hosts` file, but this became unscalable.
- **Solution**: DNS is a hierarchical, domain-based naming system defined in RFCs 1034 and 1035.

### DNS Architecture
- **Root Servers**: Root DNS servers form the top of the DNS hierarchy, with subsequent layers for domains (e.g., `.com`, `.org`).
- **Local Name Servers**: Each ISP or organization has a local DNS server to handle queries, which reduces lookup latency for commonly requested hostnames.

### DNS Functions
- **Translation**: Converts names to IP addresses and vice versa.
- **Mail Resolution**: Resolves mail domains and servers for e-mail delivery.

---

## 5. DNS Name Resolution Types
- **Standard Name Resolution**: Maps a hostname to an IP address.
- **Reverse Name Resolution**: Maps an IP address to a hostname.
- **Electronic Mail Resolution**: Maps e-mail domains to mail servers.

### Authoritative DNS Servers
- **Definition**: DNS servers that provide authoritative mappings for a domain’s IP addresses (e.g., for an organization’s web and mail servers).

### Local Name Servers
- **Function**: Acts as a proxy to forward DNS queries into the hierarchy, reducing lookup times.
- **Example**: Google’s public DNS server can serve as a local name server (e.g., 8.8.8.8).

---

## 6. Peer-to-Peer (P2P) Applications

### Overview
- **Model**: Diverges from the client-server model; in P2P, all nodes (peers) have equal status.
- **Function**: For a specific transaction, one peer acts as the client and the other as the server.
- **Common Applications**:
  - **File Sharing**: Sharing files directly between peers.
  - **Instant Messaging**: Communication between users without a central server.
  - **Online Gaming**: Enables direct connections between players.
  - **Distributed Services**: Decentralized services such as blockchain.

---

## 7. P2P File Sharing

### Example Process
1. **Peer Connection**: A user (Alice) runs a P2P client and connects to other peers.
2. **Search**: Alice searches for a file (e.g., "Hey Jude").
3. **Download**: The application finds peers with the file, and Alice selects one peer (Bob) to download from.
4. **Upload Sharing**: While downloading, Alice may also upload parts of the file to other peers.

### Advantages of P2P File Sharing
- **Scalability**: Every peer can serve as both client and server, creating a scalable network.

---

## 8. Centralized Directory in P2P (Example: Napster)
- **Process**:
  1. Each peer informs a central server of its IP and available files.
  2. The server maintains a directory of peers and files.
  3. Peers query the central server to locate files.
- **Limitations**:
  - **Single Point of Failure**: If the server fails, the network is disrupted.
  - **Performance Bottleneck**: Centralized structure limits scalability.

---

## 9. Decentralized File Sharing (Example: BitTorrent)

### BitTorrent Protocol
- **Mechanism**: Distributes files using a "swarm" model.
- **File Preparation**: The file to be shared is broken into pieces, and a `.torrent` file is created, containing:
  - **Metadata**: Information about the file.
  - **Tracker Info**: Location of the tracker that coordinates file distribution.

### File Download Process
1. **Obtain .torrent**: Users download a `.torrent` file from a website.
2. **Connect to Tracker**: The tracker directs users to peers with file pieces.
3. **Download Pieces**: Each piece is downloaded from various peers, creating multiple replicas.

### Key Terms
- **Seeder**: A peer with the complete file.
- **Leecher**: A peer that is downloading the file.
- **Tracker**: The server that coordinates which peers have which pieces of the file.

---

## 10. Summary
- **File Servers**: Enable storage and access of files over a network.
- **Domain Name Service (DNS)**: Converts human-readable hostnames to IP addresses.
- **Peer-to-Peer (P2P)**: Allows direct data exchange between peers without a central server, supporting applications like file sharing and instant messaging.

