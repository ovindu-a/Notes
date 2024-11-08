# Wireless Networks

---

## Lesson Outcomes
After completing this lesson, you should be able to:
1. Explain wireless networking concepts (encoding, media access control).
2. Describe the IEEE 802.11 standards.
3. Explain mobile telecommunications operations.

---

## 1. Why Wireless?
- **Mobile Devices**: Devices can move within or across premises.
- **Nomadic Access**: Users work from multiple locations.
- **Ad Hoc Networking**: Temporary peer-to-peer networks, e.g., sharing documents in a meeting.

### Challenges in Wireless (Compared to Wired Networks)
- Node location tracking.
- Addressing and routing services.
- Issues like path loss, fading, interference, and multipath propagation.
- Handoff and hidden terminal problems.

---

## 2. Wireless LAN Technologies

### Spread Spectrum
- **Definition**: A method of encoding where the signal spreads over a wider bandwidth, reducing susceptibility to jamming.
- **Benefit**: Allows multiple users to share the same spectrum using different codes.

#### Types of Spread Spectrum
- **Frequency Hopping Spread Spectrum (FHSS)**: Rapidly changes frequencies within the channel.
- **Direct Sequence Spread Spectrum (DSSS)**:
  - Represents each data bit as multiple bits (chips) in the transmitted signal using a spreading code.
  - Uses XOR with a pseudorandom spreading code to spread the data signal.

### Code Division Multiple Access (CDMA)
- **Function**: A multiplexing technique used with spread spectrum, where each user has a unique chipping code.
- **Process**:
  1. Data bits are converted into chips based on a unique chipping code.
  2. Chips are transmitted, with orthogonal codes to prevent interference between users.

---

## 3. IEEE 802.11 Standards (Wi-Fi)

### 802.11 Terminology
- **BSS (Basic Service Set)**: A group of devices using the same MAC (Medium Access Control) protocol within a wireless medium.
- **DS (Distribution System)**: Connects multiple BSSs to create an ESS (Extended Service Set).
- **IBSS (Independent Basic Service Set)**: A self-contained network without access to a distribution system (ad hoc network).

### 802.11 Architecture
- **Infrastructure Mode**: Uses base stations (e.g., cell towers, access points) to provide services like addressing and routing.
- **Ad Hoc Networks**: Peer-to-peer networks without infrastructure support (IBSS).
- **Handoff**: Transition from one base station to another during movement.

### 802.11 Medium Access Control (MAC)
- **DFWMAC (Distributed Foundation Wireless MAC)**: Uses both distributed (DCF) and centralized (PCF) access control.
  - **DCF (Distributed Coordination Function)**: Uses CSMA/CA (Carrier Sense Multiple Access/Collision Avoidance) for distributed access control.
  - **PCF (Point Coordination Function)**: Uses polling for centralized access control.

### IEEE 802.11 Standards (Examples)
- **802.11a**: 5 GHz band, OFDM (Orthogonal Frequency Division Multiplexing), speeds up to 54 Mbps.
- **802.11b**: 2.4 GHz band, DSSS, speeds of 5.5 and 11 Mbps.
- **802.11g**: Extends 802.11b with speeds >20 Mbps, up to 54 Mbps.
- **802.11n**: Higher throughput using MIMO (Multiple Input, Multiple Output), supports 2.4 GHz and 5 GHz bands.

---

## 4. IEEE 802.11 Frame Structure
- **Frame Fields**:
  - **Address 1**: MAC (Medium Access Control) address of the receiver.
  - **Address 2**: MAC address of the transmitter.
  - **Address 3**: Interface address of the router connecting the BSS to other networks.
  - **Address 4**: Used in ad hoc mode.

---

## 5. Mobile Telecommunications

### Mobile Telecom Generations
| Generation | Year | Services              | Data Rates       | Multiplexing | Core Network |
|------------|------|-----------------------|------------------|--------------|--------------|
| 1G         | 1984 | Analog voice          | 1.9 kbps        | FDMA (Frequency Division Multiple Access)         | PSTN (Public Switched Telephone Network)         |
| 2G         | 1991 | Digital voice         | 14.4 kbps       | TDMA (Time Division Multiple Access), CDMA       | PSTN         |
| 3G         | 2002 | Broadband data        | 2 Mbps          | CDMA         | Packet-based |
| 4G         | 2010 | IP-based, high-speed  | 200 Mbps        | OFDMA (Orthogonal Frequency Division Multiple Access)        | IP backbone  |
| 5G         | 2019 | Beyond voice & data   | 20 Gbps         | OFDMA        | IP backbone  |

### Components of a Mobile Communication System
- **Base Station**: Fixed infrastructure.
- **Mobile Station**: User device.
- **RF (Radio Frequency) Channels**: Uses paired channels for uplink (mobile to base) and downlink (base to mobile).

### Types of Mobile Communication Systems
- **Cordless Telephone Systems**: Short range, low capacity.
- **Cellular Systems**: High capacity, public networks.
- **Mobile Satellite Systems**: Long-range communication, ideal for remote areas.

### The Cellular Concept
- **Principles**:
  - **Low-power transmitters**: Reduce interference.
  - **Frequency Reuse**: Allows channel reuse across cells.
  - **Cell Splitting**: Increases capacity in high-traffic areas.
  - **Handoff**: Transfers the connection from one base station to another.
  - **Central Control**: Managed by the MTSO (Mobile Telecommunications Switching Office).

### Cellular System Architecture
- **RF Channels**:
  - **Voice Channels**: For communication.
  - **Control Channels**: For system control.
- **Multiple Access Techniques**:
  - **FDMA (Frequency Division Multiple Access)**: Divides spectrum into separate frequency channels.
  - **TDMA (Time Division Multiple Access)**: Divides access by time slots.
  - **CDMA (Code Division Multiple Access)**: Uses unique codes for each user.

---

## 6. Cellular System Operation

### Key Processes
- **Mobile Initialization**: Finds and connects to the strongest control channel.
- **Call Origination and Termination**: Manages call setup and termination.
- **Handoff**: Moves the call to a new base station as the user moves.
- **Power Control**: Adjusts transmission power based on signal strength.
- **Location Updating**: Updates the subscriber’s location in the HLR (Home Location Register) or VLR (Visitor Location Register).
