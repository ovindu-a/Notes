# Data Transmission

### Instructor Information
- **Instructor**: Sunimal Rathnayake, CS2033 – Data Communication and Networking
- Based on materials by Prof. Gihan Dias and Dr. Sulochana Sooriyaarachchi, and *Data and Computer Communications* by William Stallings.

---

## Outline
1. **Transmission Modes**: Parallel and Serial Transmission
2. **Multiplexing**: Frequency Division, Synchronous Time Division, Statistical Time Division, and ADSL (Asymmetric Digital Subscriber Line)

---

## Transmission Modes

### 1. Parallel Transmission
- **Definition**: Multiple bits are transmitted simultaneously, with each bit having its own dedicated channel or line. 
- **Mechanism**: A group of bits (often 8 bits for a byte) is sent all at once over separate lines.
- **Pros**:
  - **Speed**: Parallel transmission is fast as multiple bits are sent simultaneously, making it ideal for short-distance, high-speed communication (e.g., computer buses).
- **Cons**:
  - **Distance Limitations**: Over longer distances, maintaining synchronization becomes challenging, as bits may not arrive simultaneously (known as skew).
  - **Cost and Complexity**: Requires more wires or channels for each bit, increasing the overall cost and complexity.
  - **Signal Integrity**: Over longer distances, parallel cables are prone to signal degradation, interference, and crosstalk between channels, which can distort the signal.
- **Applications**: Primarily used within devices or systems where short distances are involved, such as within a computer's motherboard or between peripheral devices.

### 2. Serial Transmission
- **Definition**: Bits are transmitted sequentially over a single channel or line.
- **Mechanism**: Data is broken down and transmitted one bit at a time, in a continuous stream.
- **Pros**:
  - **Reliability**: Fewer wires or channels are needed, making it more reliable for long-distance communication.
  - **Cost-Effective**: Reduces the cost of cabling and is less prone to issues like crosstalk and signal degradation.
- **Cons**:
  - **Slower for Short Distances**: Serial transmission may be slower than parallel for short distances due to sequential transmission.
  - **Complexity in Synchronization**: Requires careful synchronization between sender and receiver to ensure the correct order of bits.
- **Applications**: Used in long-distance communication systems (e.g., USB, Ethernet), where speed and cost-efficiency are critical.

---

## Types of Serial Transmission

1. **Asynchronous Transmission**:
   - **Description**: Data is divided into small groups, like bytes, which are sent independently rather than as a continuous stream.
   - **Characteristics**:
     - Each byte or small data group includes a **start bit** and **stop bit(s)** to indicate the beginning and end of the transmission.
     - **Start Bit**: Changes the line from idle (usually representing binary 1) to 0, signaling the start of a transmission.
     - **Stop Bit**: Changes the line back to the idle state (binary 1) after transmission.
   - **Pros**:
     - Flexible timing; the receiver does not need to know when the next group of bits will arrive.
     - Simple and low-cost, making it ideal for devices that transmit data intermittently.
   - **Cons**:
     - **Overhead**: Additional start and stop bits add overhead, reducing data transmission efficiency.
   - **Applications**: Used in keyboard communication, where data is sent in short bursts.

2. **Synchronous Transmission**:
   - **Description**: Data is sent in larger, continuous blocks called **frames** without start and stop bits for each byte.
   - **Characteristics**:
     - Frames contain **synchronization bits**, **control bits**, **data bits**, **error-checking bits**, and **end-of-frame bits**.
     - **Frame Synchronization**: Necessary to maintain timing between the sender and receiver.
   - **Pros**:
     - More efficient than asynchronous, as it eliminates redundant start and stop bits.
     - Suitable for high-speed data transfer with fewer timing-related errors.
   - **Cons**:
     - Complex setup; requires precise synchronization, which may increase costs.
   - **Applications**: Used in network communications, such as Ethernet, where large volumes of data are transmitted.

3. **Isochronous Transmission**:
   - **Description**: Combines features of asynchronous and synchronous transmission, where data is sent in regular intervals but allows for time-sensitive delivery.
   - **Characteristics**:
     - Guarantees a consistent data rate, ensuring data is delivered at specific time intervals.
     - Often used in systems that require real-time data transmission with minimal delay.
   - **Applications**: Ideal for audio and video streaming, where data needs to be delivered in a steady stream.

---

## Simplex, Half-Duplex, and Full Duplex

- **Simplex**: Data flows in only one direction. Used in systems where feedback is not necessary, such as broadcasting (e.g., television).
- **Half-Duplex**: Data can flow in both directions, but only one direction at a time. Typical in two-way radio communication (e.g., walkie-talkies).
- **Full Duplex**: Data can flow in both directions simultaneously, enabling interactive communication, as seen in telephones.

---

## Multiplexing

Multiplexing allows multiple data streams to share a single communication medium, improving bandwidth usage.

### 1. Frequency Division Multiplexing (FDM)
   - **Concept**: Different signals are assigned distinct frequency bands within the available bandwidth.
   - **Process**:
     - Each signal is modulated onto its own carrier frequency, known as a **subcarrier**.
     - Modulated signals are combined to form a composite baseband signal that can be transmitted over a single medium.
   - **Applications**: Widely used in radio and TV broadcasting, where each station operates on a different frequency.
   - **Issues**:
     - **Crosstalk**: Overlapping spectra can cause interference between channels.
     - **Intermodulation Noise**: Occurs in long-distance transmissions due to non-linearities in amplifiers.
   - **Special Case – Wavelength Division Multiplexing (WDM)**:
     - Used in fiber optics to send multiple light wavelengths (colors) over a single fiber.
     - Enables very high data rates by allowing each wavelength to carry its own data stream.

### 2. Synchronous Time Division Multiplexing (TDM)
   - **Concept**: Time on a single transmission channel is divided into fixed intervals (time slots), each assigned to a specific data source.
   - **Process**:
     - Data from each source is interleaved in these time slots, creating a composite data stream.
     - Each source gets a fixed time slot, whether or not it has data to transmit.
   - **Pros**:
     - Simple implementation, as each source is guaranteed access to the channel at regular intervals.
   - **Cons**:
     - **Inefficiency**: Time slots are wasted if a source has no data to send.
   - **Applications**: Used in telecommunications and digital voice transmission.

### 3. Statistical Time Division Multiplexing (STDM)
   - **Concept**: Dynamically allocates time slots to sources based on demand, reducing wasted bandwidth.
   - **Process**:
     - The multiplexer checks which sources have data to send and fills the frame accordingly.
     - The frame is sent only when filled, improving channel utilization.
   - **Pros**:
     - More efficient than synchronous TDM, as time slots are used only when needed.
   - **Cons**:
     - Complexity in managing dynamic time slot allocation and ensuring correct data delivery.
   - **Applications**: Ideal for environments with sporadic data transmission, such as terminal-to-mainframe connections.

---

## Asymmetric Digital Subscriber Line (ADSL)

ADSL is a form of digital subscriber line technology that provides high-speed internet access over existing telephone lines, optimizing available bandwidth.

- **Asymmetry**: ADSL provides higher data rates downstream (to the user) than upstream (from the user).
- **Frequency Division Multiplexing (FDM)**:
  - The frequency spectrum is divided as follows:
    - **POTS (Plain Old Telephone Service)**: The 0-4 kHz band is reserved for traditional voice service.
    - **Upstream and Downstream Bands**: Use the remaining spectrum for digital data, with a larger portion allocated for downstream.
- **Echo Cancellation**:
  - An alternative to FDM that allows bidirectional data transmission within the same frequency band by canceling echoes of the transmitted signal.
- **Discrete Multitone (DMT)**:
  - Divides the transmission band into smaller 4 kHz subchannels.
  - Each subchannel is tested for signal quality, and higher-quality channels carry more bits, optimizing data throughput.

---

## Summary

Data transmission encompasses different modes (parallel vs. serial) and directions (simplex, half-duplex, full-duplex). Multiplexing techniques like FDM, TDM, and STDM allow efficient use of a single channel by sharing bandwidth among multiple signals. Technologies like ADSL leverage these techniques to provide high-speed internet over existing infrastructure. Understanding these concepts is essential for designing efficient and reliable communication systems.