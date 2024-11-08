# Transmission Errors

### Instructor Information
- **Instructor**: Sunimal Rathnayake, CS2033 – Data Communication and Networking
- Reference: *Data Communications and Computer Networks: A Business User’s Approach* by Curt M. White

---

## Overview of Transmission Errors

- **Transmission Errors**: Errors occur when data signals are distorted, altered, or lost during transmission due to noise or interference.
- **Focus on Data Link Layer**: Error detection and correction primarily take place in the Data Link Layer, ensuring reliable data transfer independent of the physical medium.

---

## Types of Noise and Errors

Noise is a primary cause of transmission errors, with different types affecting signal quality in various ways:

### 1. White Noise (Thermal or Gaussian Noise)
   - **Description**: Constant, relatively predictable noise caused by random electron motion.
   - **Effect**: If strong, it disrupts the signal entirely.
   - **Solution**: Can often be minimized but not fully eliminated.

### 2. Impulse Noise
   - **Description**: Sudden, unpredictable spikes in power that can destroy multiple bits of data.
   - **Effect**: Harder to remove from analog signals, especially damaging for fast transmissions.
   - **Example**: Electrical spikes from lightning or power surges.

### 3. Crosstalk
   - **Description**: Unwanted coupling between signal paths, resulting in interference.
   - **Effect**: Example includes hearing a different conversation on a phone line.
   - **Solution**: Reduced with proper cable design and shielding.

### 4. Echo
   - **Description**: Reflected feedback of a transmitted signal, common in coaxial cables.
   - **Effect**: Strong echo can interfere with the original signal.
   - **Solution**: Minimized by using cable termination techniques and quality coaxial cables.

### 5. Jitter
   - **Description**: Small timing irregularities in digital signal transmission.
   - **Effect**: Severe jitter forces systems to slow down to synchronize data.
   - **Solution**: Improved shielding and stable transmission equipment.

### 6. Delay Distortion
   - **Description**: Different frequencies in a signal travel at different speeds through the medium.
   - **Effect**: Results in a distorted signal, with successive bits merging.
   - **Solution**: Use of equalizers to align propagation speeds.

### 7. Attenuation
   - **Description**: Loss of signal strength as it travels over distance.
   - **Effect**: If too weak, the signal becomes unreadable.
   - **Solution**: Use amplifiers or repeaters and select low-loss media.

### 8. Interference
   - **Description**: External signals interfere with transmission, often intermittently.
   - **Effect**: Reduces signal clarity and can be challenging to diagnose.
   - **Solution**: Proper shielding and avoiding interference sources.

---

## Error Prevention Techniques

To reduce the likelihood of errors, various preventive techniques are employed:

1. **Shielding**: Protects cables from external interference.
2. **Line Conditioning and Equalization**: Optimizes telephone lines and other media.
3. **Media and Equipment Upgrades**: Replacing older, noisy components with newer, digital technology.
4. **Repeaters and Amplifiers**: Boosts signal strength over long distances.
5. **Capacity Management**: Ensures media are not overloaded, maintaining signal integrity.

---

## Error Detection Techniques

Error detection identifies when errors occur in data transmission. Methods include:

### 1. Information Redundancy and Coding
   - **Concept**: Adding extra bits to data (coding) helps detect errors.
   - **Data Word to Codeword**: A data word with `d` bits is encoded into a `c`-bit codeword, where `c > d`.
   - **Detection**: If the received codeword is invalid, an error is detected.
   - **Correction**: Some coding schemes can correct detected errors.

### 2. Parity Codes
   - **Types**:
     - **Even Parity**: The parity bit is set so the total number of `1`s is even.
     - **Odd Parity**: The parity bit makes the total number of `1`s odd.
   - **Example**: `10011001` with even parity bit added becomes `100110010` if it has an even count of `1`s.
   - **2D Parity Check (VRC)**: Two-dimensional parity detects a single erroneous bit by checking row and column parities.

### 3. Hamming Distance
   - **Definition**: The Hamming distance between two codewords is the number of differing bit positions.
   - **Application**: Higher Hamming distances between valid codewords enhance error detection and correction capabilities.

### 4. Hamming Code
   - **Concept**: Based on the Hamming distance, it uses multiple parity bits to detect and correct errors.
   - **(7,4) SEC Hamming Code**: A 7-bit code with 4 data bits and 3 parity bits, capable of correcting single-bit errors.
   - **Calculation**:
     - **Parity Bit Formula**: \(2^r \geq m + r + 1\), where \(r\) is the number of parity bits and \(m\) is the number of data bits.

### 5. Cyclic Redundancy Check (CRC)
   - **Description**: A non-separable code treating data as a polynomial, which is divided by a generating polynomial.
   - **Operation**:
     - **Transmitter**: Divides the data polynomial by the generator polynomial, appending the remainder as a checksum.
     - **Receiver**: Divides the received data by the same polynomial. A remainder of zero indicates no error.
   - **Example**:
     - **Message**: `101101`
     - **CRC Polynomial**: \(x^3 + x^2 + 1\) (binary: `1101`).
     - **Calculation**: Using Modulo-2 long division, the remainder becomes the CRC appended to the message.

---

## Error Control

Error control methods manage errors detected in transmission, either by requesting retransmission or correcting errors on the fly.

- **Retransmission**: Requests data resend when errors are detected.
- **Forward Error Correction (FEC)**: Corrects errors in real-time using additional error-correcting codes.

---

### Summary

In data communication, error prevention, detection, and correction are essential to ensure data integrity and reliability. Common techniques include:

- **Error Prevention**: Shielding, line conditioning, capacity management.
- **Error Detection**: Parity codes, Hamming codes, and CRC.
- **Error Correction**: Hamming code (e.g., (7,4) SEC) and Forward Error Correction for real-time applications.

This framework enhances data reliability across noisy and interference-prone channels, supporting robust communication in complex network environments.