# Telephony and Multimedia

### Author: Sunimal Rathnayake, CS2033 - Data Communication and Networks
**With material from Prof. Gihan Dias**

---

## Lesson Topics
This lesson covers:
1. Telecommunications (voice, video, and data).
2. The Telephone Network and its components.
3. Enhanced telecommunication services.
4. Voice over IP (VoIP) technology.
5. Multimedia concepts and networking.

---

## 1. Telecommunications

### Types of Telecommunications
- **Voice**:
  - **Telephony**: Point-to-point communication between two parties.
  - **Conferencing**: Multi-party communication.
  - **Radio Broadcast**: One-to-many voice transmission.

- **Video**:
  - **Video Calls**: Point-to-point or multi-party video communication.
  - **Streaming and Television**: Delivery of video content to multiple viewers.

- **Data**: Transmission of digital data over communication networks.

---

## 2. The Telephone Network

### Components of the Telephone Network
- **Access Network**: Provides connection from subscribers to the local exchange (central office, CO).
  - **Significance**: The access network represents the largest investment and bottleneck in telecommunication systems.

### Access Technologies
- **Local Loop**: Copper wire pairs carrying analog voice.
- **Wireless Local Loop (WLL)**: Wireless replacement of the local loop.
- **Digital Subscriber Loop (DSL)**: Supports both data and voice over copper wires.
- **Fiber to the x (FTTx)**: Optical fiber connections to the curb, business, or home.

---

## 3. Switching and Transmission in Telephony

### Switching
- **Purpose**: Connects subscribers on demand.
- **Types of Switches**:
  - **Manual Operators**: Early form of switch management.
  - **Automatic Switches**: Uses electromechanical or software-controlled switches.

### Transmission
- **Function**: Transports signals between network subscribers.
- **Methods**: High-capacity copper cables, microwave (radio) links, optical fibers.
- **Capabilities**: Carries thousands of multiplexed calls between exchanges.

---

## 4. Signalling in Telephony
- **Functions**:
  - **Call Connection and Disconnection**: Manages the start and end of calls.
  - **Billing**: Tracks call details for billing purposes.
  - **Subscriber Loop Signalling**: Provides dial tone, dialed digits, and ringing signals.
  - **Inter-exchange Signalling**: Controls connections between exchanges for routing calls.

---

## 5. Telephone Numbering System
- **Structure**:
  - **Country Code**: E.g., 94.
  - **Area Code**: E.g., 11.
  - **Operator Code**: E.g., 2.
  - **Telephone Number**: E.g., 650301.
  - **Extension**: E.g., 3100.

---

## 6. Enhanced Telecommunication Services

### Common Services
- **Short Message Service (SMS)**: 
  - Allows sending and receiving of short messages (up to 160 characters).
  - Uses Store and Forward Service through SMS Center.

- **Calling Line Identification (CLI)**:
  - Displays the caller's number to the receiver.
  - Available on both ISDN (Integrated Services Digital Network) and analog lines.
  - Can be enhanced by matching numbers with directory entries.

- **Other Services**:
  - **Conference Calls**: Multiple parties on a single call.
  - **Call Forwarding**: Redirects incoming calls to another number.
  - **Voice Mail**: Stores voice messages for later retrieval.
  - **Follow Me**: Redirects calls based on user's location.
  - **Short Codes**: Special numbers for quick access (e.g., 1919 for information).

### Location-Based Services (LBS)
- **Description**: Services that vary based on subscriber’s location.
  - **Examples**: Emergency services (e.g., 119), delivery services.
- **Technology**:
  - For fixed lines: Location is known.
  - For mobile phones: Location identified by **Cell ID**, **GPS (Global Positioning System)**, or **Triangulation**.

---

## 7. Voice over IP (VoIP)

### What is VoIP?
- **Definition**: Uses packet-switched data networks for voice communication.
- **Supported Networks**: Ethernet, WiFi, 3G, 4G, or any IP-based network.
- **Alternative Name**: Also known as Internet Telephony.

### Why VoIP?
- **Integration**: Combines data, multimedia, and voice on one network.
- **Cost Savings**: Reduces the need for separate voice networks, lowers costs locally and internationally.

### How VoIP Works
1. **Audio Capture**: User speaks into a microphone.
2. **Encoding**: Voice converted to digital format by a codec (coder-decoder).
3. **Packetization**: Digital voice data is split into packets for network transmission.
4. **Playback**: Receiving device decodes packets back to audio and plays it.

### VoIP Advantages
- Uses existing data networks.
- Supports integration with applications and advanced features (e.g., video, conferencing).

### VoIP Disadvantages
- Higher latency (delay).
- Potential packet loss.
- Variable voice quality.

---

## 8. Multimedia

### What is Multimedia?
- **Definition**: Integration of text, graphics, images, video, animation, and sound.
- **Characteristics**:
  - **Digital Format**: Multimedia content is typically digital.
  - **Multiple Media Types**: Often combines audio and video.
  - **Interactivity**: Can be interactive (e.g., video games) or non-interactive (e.g., movies).

### Media Types
- **Text**: Plain (ASCII, Unicode) or rich text (HTML).
- **Graphics**: Vector-based images (lines, curves, shapes).
- **Images**: 2D pixel-based visuals with varying bit depths.
- **Video and Animation**:
  - **Video**: Moving images created from a series of bitmap frames.
  - **Animation**: Computer-generated moving graphics.
- **Sound**:
  - **Natural Sound**: Recorded audio signals.
  - **Structured Sound**: Synthesized sounds (e.g., MIDI files).

---

## 9. Multimedia Networking

### Classes of Multimedia Applications
- **Streaming Stored Multimedia**:
  - Example: YouTube.
  - Allows pause, rewind, and fast-forward.

- **Streaming Live Multimedia**:
  - Example: Live radio or sports events.
  - Playback often lags behind real-time but follows timing constraints.

- **Real-Time Interactive Multimedia**:
  - Example: IP telephony, video conferencing.
  - End-to-end delay requirements: Less than 150 ms for audio is ideal; up to 400 ms is acceptable.