# Switching in Networks

Switching is the technique used to route data across a network from sender to receiver, especially when nodes aren't directly connected. There are various switching methods, each suited to different networking requirements.

## Types of Switching

1. **Circuit Switching**
   - **Definition**: Establishes a dedicated communication path between two endpoints for the duration of the session.
   - **Example**: Traditional landline telephones use circuit switching, where a dedicated path is created and maintained throughout a call.
   - **Pros**: Low transmission delay once the circuit is set.
   - **Cons**: Inefficient for bursty data (e.g., computer communications) due to potential idle time.

2. **Message Switching**
   - **Definition**: Entire messages are sent from node to node in a store-and-forward manner, without a dedicated path.
   - **Example**: Early telegraph systems and email systems where messages are held temporarily at each node until the next node becomes available.
   - **Pros**: No need for dedicated path setup.
   - **Cons**: Messages can experience significant delays if the network is congested.

3. **Packet Switching**
   - **Definition**: Data is divided into packets, which are routed independently through the network.
   - **Types**:
     - **Virtual Circuit Switching**: Establishes a predefined route for packets; all packets in a session follow the same path. Example: Frame Relay networks.
     - **Datagram Switching**: Packets are routed individually and may take different paths, adapting to network changes. Example: The Internet uses datagram switching.
     - **Label Switching**: A label is attached to each packet, and core switches use this label to route packets efficiently. Example: MPLS (Multiprotocol Label Switching) in modern WANs.
   - **Pros**: Efficient use of network resources; suitable for data networks.
   - **Cons**: Potential for packet delay or reordering, as packets may take different paths.

## Comparison Table

| Switching Type         | Dedicated Path | Delays             | Use Cases                              |
|------------------------|----------------|--------------------|----------------------------------------|
| Circuit Switching      | Yes            | Setup delay, low during transmission | Landline telephony                     |
| Message Switching      | No             | High if network congested | Early email and telegraph systems     |
| Packet Switching       | No             | Low to moderate, adaptive | Internet, modern data communications   |

This summary captures the key points and differences in switching techniques, along with real-world examples to illustrate their applications.