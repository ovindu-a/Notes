# Transmission Media

### Instructor Information
- **Instructor**: Sunimal Rathnayake, CS2033 – Data Communication and Networking
- Based on materials by Prof. Gihan Dias and Dr. Sulochana Sooriarachchi

---

## Lesson Outcomes
- **Objectives**:
  - Categorize different transmission media technologies.
  - Explain the key principles of transmission media.

---

## Characteristics of Transmission Media

- **Key Factors**:
  - **Cost**: Varies depending on type and installation.
  - **Data Rate**: Influenced by medium bandwidth.
  - **Bandwidth**: Higher bandwidth allows higher data rates.
  - **Transmission Impairments**:
    - **Attenuation**: Loss of signal strength over distance.
    - **Dispersion and Reflection**: Signal scattering and bouncing.
  - **Interference**: Caused by external factors like motors, lightning, or nearby wires.

---

## Guided Transmission Media

Guided media direct signals through physical pathways, which include copper cables and optical fibers.

### 1. Twisted Pair Cables
- **Composition**: Copper wires twisted together to reduce interference.
- **Types**:
  - **UTP (Unshielded Twisted Pair)**: Common in telephones, low-cost, but susceptible to interference.
  - **STP (Shielded Twisted Pair)**: Shielded to reduce interference, more expensive and bulkier.
- **Properties**:
  - **Crosstalk**: Reduced by twisting, which minimizes signal interference between pairs.
  - **Attenuation**: Signal loss over longer distances.

### 2. Coaxial Cable
- **Structure**: Copper core with a metallic shield to protect against electromagnetic interference.
- **Modes**:
  - **Baseband**: Single data stream.
  - **Broadband**: Multiple signals on multiple channels.
- **Usage**: Widely used for cable TV and early internet connections.

### 3. Optical Fiber
- **Function**: Uses light waves instead of electricity, allowing long-distance transmission with high bandwidth.
- **Components**:
  - **Core and Cladding**: Light is transmitted through the core, reflecting at the cladding boundary.
  - **Light Source**: LEDs or lasers.
- **Types**:
  - **Single-Mode Fiber**: Narrow core, supports one light path, ideal for long distances.
  - **Multimode Fiber**:
    - **Step-Index**: Multiple light paths but suffers from modal dispersion.
    - **Graded-Index**: Reduces dispersion by gradually changing core density.
- **Advantages**:
  - **High Capacity**: Supports high data rates.
  - **Immunity to Electrical Noise**: Not affected by electromagnetic interference.
  - **Environmental Resistance**: Resilient to humidity and temperature variations.

---

## Unguided Transmission Media

Unguided media transmit data through the air or free space without a physical conductor, including wireless technologies.

### 1. Electromagnetic Spectrum
- **Types of Frequencies**:
  - **Microwave (2-40 GHz)**: Highly directional, used for point-to-point and satellite communications.
  - **Radio (30 MHz - 1 GHz)**: Omnidirectional, used for FM radio and broadcast TV.
  - **Infrared (300 GHz - 400 THz)**: Local, line-of-sight applications like remote controls.

### 2. Antennas
- **Function**: Convert electrical signals to electromagnetic waves and vice versa.
  - **Transmission Antenna**: Radiates radio frequency energy.
  - **Reception Antenna**: Converts electromagnetic energy back to radio frequency.
- **Types**:
  - **Isotropic Antenna**: Theoretical model that radiates equally in all directions.
  - **Parabolic Antenna**: Reflects signals for focused transmission, commonly used in satellite dishes.

### 3. Terrestrial Microwave
- **Use**: Long-distance and point-to-point communication.
- **Properties**:
  - **Frequency Range**: 1-40 GHz.
  - **Requirements**: Line of sight between antennas; signal loss can occur due to distance and atmospheric conditions.
- **Applications**: Telecommunications, backbone network links.

### 4. Satellite Microwave
- **Function**: Satellites act as relay stations, receiving signals and retransmitting them.
- **Orbit Types**:
  - **Geostationary Orbit**: Fixed position relative to Earth; supports consistent signal coverage.
  - **LEO (Low Earth Orbit) and MEO (Medium Earth Orbit)**: Used for mobile and GPS applications.
- **Uses**: Television broadcasting, GPS, long-distance phone networks.

### 5. Broadcast Radio
- **Frequency Range**: 30 MHz - 1 GHz.
- **Characteristics**:
  - **Omnidirectional**: Suitable for broadcasting over wide areas.
  - **Line of Sight**: Limited by obstacles and multipath interference.

### 6. Infrared Transmission
- **Usage**: Short-range, line-of-sight communication, commonly found in remote controls.
- **Properties**:
  - **Reflection-Based Transmission**: Blocked by physical barriers like walls.
  - **No Licensing Required**: Unlike many radio frequencies.

---

## Wireless Propagation Modes

### 1. Ground Wave Propagation
- **Range**: Low to medium frequencies (100-1000 kHz).
- **Behavior**: Waves follow the Earth’s curvature, enabling transmission despite obstacles.

### 2. Sky Wave Propagation
- **Range**: High frequencies (1-30 MHz).
- **Behavior**: Signals are refracted by the ionosphere, bouncing back to Earth for long-distance communication.

### 3. Line-of-Sight Propagation
- **Range**: High frequencies (above 30 MHz).
- **Requirement**: Clear line of sight; antenna height can extend range.
- **Challenges**: Signal loss due to atmospheric absorption, multipath interference, and refraction.

---

## Signal Interference and Loss

- **Free Space Loss**: Signal strength diminishes over distance.
- **Multipath Interference**: Multiple signal reflections cause delays, leading to signal distortion.
- **Atmospheric Absorption**: Water vapor and oxygen absorb certain frequencies, reducing signal strength.

---

## Transmission Media Standards

- **V-Series**: Telephone communication standards.
- **X-Series**: Interface standards by CCITT (International Consultative Committee for Telephony and Telegraphy).
- **EIA (Electronic Industries Alliance)**: Defines physical connections and data transfer standards.
- **IEEE (Institute of Electrical and Electronics Engineers)**: Sets standards for LAN, WAN, and wireless, such as IEEE 802.

---

This document provides an in-depth understanding of both guided and unguided transmission media, detailing their properties, uses, and limitations, as well as key technical standards that govern data communication protocols.