# Encoding and Modulation

### Instructor Information
- **Instructor**: Sunimal Rathnayake, CS2033 – Data Communication and Networking
- Based on materials from *Data and Computer Communications* by William Stallings

---

## Introduction to Encoding Techniques

Encoding and modulation are essential processes in data communication. They define how data (digital or analog) is represented as signals (digital or analog) for transmission.

- **Encoding Types**:
  - **Digital Data, Digital Signal**: Converts binary data into discrete pulses (e.g., NRZ).
  - **Analog Data, Digital Signal**: Digitizes analog signals for digital transmission (e.g., PCM).
  - **Digital Data, Analog Signal**: Modulates binary data for transmission over analog media (e.g., ASK, FSK).
  - **Analog Data, Analog Signal**: Modulates analog data to fit specific frequencies or channels (e.g., AM, FM).

---

## Key Terms

- **Unipolar Encoding**: Uses only one voltage level.
- **Polar Encoding**: Uses both positive and negative voltage levels.
- **Modulation Rate**: Measured in baud (signal changes per second).
- **Mark and Space**: Represent binary 1 and binary 0, respectively.

---

## Encoding Schemes for Digital Data, Digital Signal

1. **Non-Return to Zero-Level (NRZ-L)**: Uses two different voltage levels for 0 and 1, maintaining a constant voltage during each bit period. Common in magnetic recording but less in transmission.
   
2. **Non-Return to Zero Inverted (NRZI)**: Changes voltage at the start of each bit period to denote binary 1, while 0s are indicated by no change.

3. **Multilevel Binary**:
   - **Bipolar-AMI (Alternate Mark Inversion)**: Uses alternating polarity for binary 1s, while 0 is represented by no voltage.
   - **Pseudoternary**: Uses voltage levels to represent 0s while 1s have no signal.

4. **Biphase Encoding**:
   - **Manchester Encoding**: Transition in the middle of each bit serves as both clock and data signal (Low to High = 1, High to Low = 0). Used in IEEE 802.3.
   - **Differential Manchester**: Mid-bit transition for clocking; transitions at the start represent 0s, and no transition represents 1s. Used in IEEE 802.5.

### Pros and Cons of Encoding Schemes
- **NRZ**:
  - **Pros**: Efficient bandwidth usage.
  - **Cons**: DC component presence, lacks synchronization.
- **Biphase**:
  - **Pros**: Synchronization due to self-clocking, no DC component.
  - **Cons**: Requires higher bandwidth due to more transitions.

---

## Scrambling Techniques

Scrambling modifies data to avoid sequences of zeros that can disrupt transmission.

- **B8ZS (Bipolar with 8-Zero Substitution)**: Based on AMI, replaces eight zeros with a specific sequence to maintain synchronization.
- **HDB3 (High-Density Bipolar 3 Zeros)**: Replaces strings of four zeros with a pattern to ensure synchronization and avoid long zero-level signals.

---

## Modulation for Digital Data, Analog Signal

Modulation allows digital data to be transmitted over analog media by altering a carrier signal’s properties.

### Modulation Techniques
1. **Amplitude Shift Keying (ASK)**: Represents binary data by altering the amplitude of the carrier wave. Prone to interference but efficient for optical fiber.
   
2. **Frequency Shift Keying (FSK)**: Uses different frequencies for 0 and 1. More resilient to errors than ASK, commonly used in LANs and radio.

3. **Phase Shift Keying (PSK)**: Changes the carrier signal’s phase to represent data.
   - **Quadrature PSK (QPSK)**: More efficient, with each phase shift representing multiple bits (e.g., 2 bits per shift).
   - **Differential PSK (DPSK)**: Represents bits by phase shifts relative to the previous bit, rather than an absolute reference.

4. **Quadrature Amplitude Modulation (QAM)**: Combines ASK and PSK to transmit multiple signals over a single channel. Common in ADSL and some wireless standards.

### Modulation Performance
- **Bandwidth**: ASK and PSK bandwidth are directly tied to bit rate, while FSK depends on the modulation frequency.
- **Error Rate**: PSK and QPSK are less error-prone than ASK and FSK in noisy environments.

---

## Analog Data, Digital Signal

### Pulse Code Modulation (PCM)
PCM digitizes analog signals by sampling them at intervals and quantizing the samples into binary values.

- **Nyquist Sampling Theorem**: A signal can be perfectly reconstructed if it is sampled at twice its highest frequency.
- **Example**: Voice signals (up to 4 kHz) are sampled at 8,000 samples per second, producing 64 kbps with 8-bit encoding.
- **Quantization**: Samples are assigned digital values, leading to some quantization noise.

### Delta Modulation (DM)
- **Approach**: Approximates the analog signal with a staircase function that moves up or down at each sample interval.
- **Application**: DM is a simpler alternative to PCM, but it may introduce distortion with complex signals.

---

## Analog Data, Analog Signal

Analog modulation of analog data enhances transmission efficiency, allowing higher frequencies for transmission over long distances.

### Modulation Types
1. **Amplitude Modulation (AM)**: Varies the carrier’s amplitude in proportion to the signal’s amplitude.
2. **Frequency Modulation (FM)**: Varies the carrier’s frequency according to the signal’s amplitude.
3. **Phase Modulation (PM)**: Shifts the carrier’s phase based on the signal.

---

## Key Takeaways

1. **Encoding and Modulation**: Essential for adapting signals for various transmission media.
2. **Encoding Techniques**: NRZ, Biphase, and Scrambling methods provide different solutions for efficient data transmission.
3. **Digital Modulation**: ASK, FSK, PSK, and QAM each have unique advantages depending on bandwidth needs and noise resistance.
4. **Analog Modulation**: AM, FM, and PM enable efficient analog data transmission over greater distances and frequencies.

This structured approach to encoding and modulation forms the foundation for reliable data transmission across diverse network types and media.