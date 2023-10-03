# Study Guide: Computer Networking Chapter 2


### Required reading
Sections: 2.1, 2.2, 2.4, 2.5, 2.6 and 2.7 

## Technology perspective

1. What are the different technologies used for connecting nodes in a computer network?

The different technologies used for connecting nodes in a computer network are:
 - Copper-Based Technologies:
   - DSL (Digital Subscriber Line): Utilizes twisted-pair copper wires for last-mile connections, providing up to 100 Mbps bandwidth. 
   - G.Fast: A copper-based technology often used within multi-dwelling apartment buildings, offering up to 1 Gbps bandwidth.
 - Fiber Optic Technology:
   - PON (Passive Optical Network): Uses optical fiber for high-speed connections, offering up to 10 Gbps bandwidth. Commonly used for connecting homes and businesses.
 - Mobile or Cellular Networks:
   - 4G (evolving into 5G): Connects mobile devices to the Internet and can serve as an Internet connection for homes and offices. Offers mobility while maintaining Internet connectivity.
 - Backbone Links:
   - Modern backbone links primarily use fiber optics and a technology called SONET (Synchronous Optical Network) for high-speed, long-distance connections between cities. Originally developed for telephone carriers.
 - Local Area Networks (LANs):
   - Ethernet and Wi-Fi: Dominant technologies used for connecting devices within a building or campus. Ethernet uses wired connections, while Wi-Fi provides wireless connectivity.


## Encoding

1. What is encoding in the context of computer networking?

Is the process of converting binary data (comprising 1s and 0s) into signals that can be transmitted over physical links in a network. Encoding is essential to ensure that the binary data from a source node can be effectively transmitted to a destination node through the network's communication channels.

2. Explain the difference between analog and digital signals.

- Analog Signals:
  - Analog signals are continuous waveforms that can take on a range of values within a given range.
  - These signals represent data as continuously varying voltage levels, frequencies, or amplitudes.
  - Analog signals are typically used in analog communication systems, such as traditional voice calls over landline phones.
  - They are susceptible to signal degradation over long distances and are more sensitive to external interference.
- Digital Signals:
  - Digital signals are discrete and represent data as a series of binary values, typically 1s and 0s.
  - These signals have distinct levels, such as high and low voltage states or on and off states.
  - Digital signals are used in digital communication systems, such as computer networks and the transmission of digital data.
  - They are less susceptible to signal degradation over long distances and are more resilient to noise and interference.


3. Explain the different types of encoding used in computer networks

- Non-Return to Zero (NRZ) Encoding:
   - NRZ encoding is a simple binary encoding scheme.
   - It maps the binary value 1 onto the high signal and the binary value 0 onto the low signal.
   - The drawback of NRZ is that it can lead to long sequences of consecutive 1s or 0s, causing issues like baseline wander, where the receiver's ability to distinguish between low and high signals is compromised due to long signal durations.

- Non-Return to Zero Inverted (NRZI) Encoding:
  - NRZI is an encoding scheme that addresses the issue of consecutive 1s in NRZ encoding.
  - In NRZI, a transition from the current signal level encodes a 1, while staying at the current signal level encodes a 0.
  - NRZI helps prevent consecutive 1s from causing problems with baseline wander.

- Manchester Encoding:
   - Manchester encoding is an encoding scheme that combines the clock signal with data signal.
   - It encodes 0 as a low-to-high transition and 1 as a high-to-low transition.
   - Manchester encoding ensures frequent signal transitions, aiding clock recovery, but it doubles the transition rate, reducing efficiency.
   - It helps the receiver maintain synchronization with the sender's clock, critical for accurate data decoding.

- 4B/5B Encoding:
  - 4B/5B encoding aims to balance efficiency and signal transitions.
  - It inserts extra bits into the data stream to break up long sequences of 0s or 1s.
  - Every 4 bits of actual data are encoded into a 5-bit code, ensuring that no more than three consecutive 0s or 1s are transmitted in a row.
  - 4B/5B encoding achieves 80% efficiency while addressing the problems of long signal durations and clock drift.

## Error Detection

1. What is error detection and why is it important in computer networks?

Error detection is the process of identifying errors or corruption in data transmitted over a computer network. It is crucial in computer networks because data can be susceptible to various forms of corruption during transmission due to factors like electrical interference, noise, or other forms of distortion. Detecting errors is essential to ensure the integrity and reliability of data

2. Explain the concept of parity checking for error detection.

It involves adding an additional bit, known as a parity bit, to a block of data. The parity bit is chosen so that the total number of 1s in the data block, including the parity bit, is either even or odd. There are two types of parity checking:

- Even Parity: The total number of 1s, including the parity bit, is made even.
- Odd Parity: The total number of 1s, including the parity bit, is made odd. 

During data transmission, if an error occurs and the number of 1s in the received data block (including the parity bit) does not match the expected parity (even or odd), an error is detected.

3. Discuss the advantages and limitations of parity checking.


Advantages of parity checking:
- Simplicity: Parity checking is straightforward to implement and requires minimal additional overhead.
- Basic Error Detection: It can detect single-bit errors effectively.

Limitations of parity checking:
- Limited Error Detection: Parity checking can only detect errors; it cannot correct them.
- Limited to Single-Bit Errors: It is only effective at detecting single-bit errors, making it inadequate for detecting multiple or more complex errors.
- Inefficiency: It is not very efficient for detecting errors in large data blocks or over noisy channels.

4. Describe the process of using checksums for error detection.

The process of using checksums for error detection are:
- 1. The sender calculates the checksum value based on the data.
- 2. The sender appends or includes the checksum in the transmitted data.
- 3. The receiver calculates its own checksum based on the received data.
- 4. The receiver compares the calculated checksum with the received checksum.
- 5. If they match, the data is assumed to be error-free; if not, an error is detected.

5. Explain Cyclic Redundancy checks. 

It uses polynomial division to generate a redundancy check value (CRC value) that is appended to the data before transmission. The receiver performs the same polynomial division on the received data and checks whether the calculated CRC value matches the received CRC value.

## Reliable Transmission

1. What is reliable transmission and why is it important in computer networks?

Is the ability of a network protocol to ensure that data sent from one node to another arrives correctly and in the right order, without errors or omissions

2. Explain the concept of stop-and-wait protocol for reliable transmission.

In this protocol, after sending a data frame, the sender waits for an acknowledgment (ACK) from the receiver. If the sender does not receive an ACK within a reasonable time (timeout), it assumes that the frame was lost or corrupted and retransmits it. The receiver acknowledges the successful receipt of each frame.

3. Discuss the advantages and limitations of stop-and-wait protocol.

- Advantages of the stop-and-wait protocol:
  - Simplicity: It is easy to understand and implement.
  - Error detection: The sender can detect lost or corrupted frames and retransmit them.
  - Flow control: It naturally provides a form of flow control since the sender waits for ACKs before sending more data.
- Limitations of the stop-and-wait protocol:
  - Inefficiency: It has low efficiency, especially on high-latency links, because the sender can have only one frame in transit at a time.
  - Limited throughput: The protocol does not fully utilize the available bandwidth, leading to underutilization of the network.
  - High latency: On high-latency links, the round-trip time for an ACK can be significant, causing delays.

4. Describe the process of using sliding window protocol for reliable transmission.

- 1. Assigning sequence numbers to each frame to maintain order.
- 2. Maintaining a send window size (SWS) that determines the number of outstanding frames the sender can transmit.
- 3. Maintaining a receive window size (RWS) on the receiver side to specify the number of out-of-order frames the receiver is willing to accept.
- 4. Using acknowledgments (ACKs) to confirm the receipt of frames and allowing the sender to advance its window.
- 5. Implementing timeouts to trigger frame retransmission in case of lost or delayed ACKs.
- 6. Handling sequence number wrapping in a finite sequence number space.


## Ethernet and Multiple Access Networks

1. What is Ethernet and how does it work?

Ethernet is a local area networking technology where multiple devices are connected to a shared communication medium, typically using twisted copper pairs or optical fibers. Each device has a unique Ethernet address (MAC address), and they communicate by sending frames over the network.

2. Explain the concept of multiple access networks.

Multiple-access networks allow multiple devices (nodes) to transmit and receive data over a shared communication medium. Nodes need to follow certain protocols to access the shared medium fairly and avoid collisions.

3. Discuss the advantages and limitations of Ethernet.

- Advantages:
    - Simplicity: Ethernet is easy to set up and administer.
    - Cost-effective: It uses inexpensive cables and network adaptors.
    - Backward compatibility: Newer Ethernet versions are backward compatible with older ones.
    - Reliable: Collision detection and retransmission mechanisms enhance reliability.
- Limitations:
    - Limited distance: Ethernet has a maximum cable length, typically around 100 meters for twisted-pair cables.
    - Limited scalability: In large networks, collision domains can become a limitation. 
    - Half-duplex communication: Traditional Ethernet operates in half-duplex mode, allowing either sending or receiving at a time.


4. Describe the process of collision detection in Ethernet.

Ethernet uses a collision detection mechanism where each transmitting node listens while it sends data. If it detects a collision, it immediately stops transmitting, sends a jamming signal, and enters a backoff period during which it waits for a random amount of time before attempting to transmit again.

5. Give examples of different multiple access techniques used in computer networks.

CSMA/CD (used in Ethernet), CSMA/CA (used in Wi-Fi networks), Time Division Multiple Access (TDMA), Frequency Division Multiple Access (FDMA), and Code Division Multiple Access (CDMA).

## Wireless Networks

1. What are wireless networks and how do they work?

Wireless networks are communication systems that use radio waves or other wireless technologies to connect devices and allow them to exchange data without the need for physical cables. In wireless networks, information is transmitted over the air through electromagnetic signals. Devices in a wireless network communicate using wireless network adapters, which include components like antennas and radios to send and receive data wirelessly.

2. Explain the concept of wireless communication channels.

Wireless communication channels are pathways through which wireless signals propagate between devices. These channels involve the transmission and reception of electromagnetic waves, typically in the radio frequency (RF) spectrum.

3. Discuss the advantages and limitations of wireless networks.

- Advantages of wireless networks:
  - Mobility: Wireless networks allow devices to connect and communicate while on the move, providing flexibility and convenience.
   - Easy deployment: Setting up wireless networks is often simpler and more cost-effective than running physical cables.
   - Scalability: Wireless networks can be easily expanded by adding more access points or devices.
   - Accessibility: Wireless networks provide connectivity in areas where laying cables is impractical.
   - Reduced clutter: Eliminating cables reduces physical clutter and simplifies network management.
- Limitations of wireless networks:
  - Interference: Wireless networks can be susceptible to interference from other wireless devices and obstacles in the environment.
  - Limited range: Wireless signals have a finite range, and signal strength decreases with distance from the access point.
  - Security concerns: Wireless networks may be vulnerable to unauthorized access if not properly secured.
  - Slower speeds: Wireless networks can have lower data transfer rates compared to wired networks.
  - Reliability: Wireless connections can be less reliable than wired connections due to signal disruptions.

4. Describe the process of wireless signal propagation and interference

- Signal Propagation:
  - Signal propagation is the process by which wireless signals travel from a transmitter to a receiver.
  - Wireless signals propagate through the air as electromagnetic waves, typically in the radio frequency (RF) spectrum.
  - The strength of a wireless signal decreases with distance from the transmitter, and it can be affected by obstacles in the environment.
- Signal Interference:
  - Signal interference is the disruption of wireless signals by other wireless devices or obstacles in the environment.
  - Interference can cause signal degradation, resulting in lower signal strength and reduced data transfer rates.
  - Interference can be caused by other wireless devices operating in the same frequency band or by physical obstacles like walls or buildings


5. Give examples of different wireless networking technologies used in computer networks.

- Wi-Fi: A wireless networking technology that uses radio waves to provide wireless connectivity to devices.
- Bluetooth: A wireless technology that uses radio waves to connect devices over short distances.
- Cellular networks: Wireless networks that provide mobile connectivity to devices over large geographical areas.
- ZigBee: A wireless technology that uses radio waves to connect devices over short distances.
- Wireless Sensor Networks (WSNs): Wireless networks that use sensors to collect data from the environment and transmit it wirelessly.

## Exercises

1. Show the Manchester, 4B/5B encoding, and the resulting NRZI signal, for the
following bit sequence:
1110 0101 0000 0011

- Manchester encoding:

  - 1 is represented as a high-to-low transition.
  - 0 is represented as a low-to-high transition.

    - 1010 1010 0101 0101

- 4B/5B encoding:
  - 1110 maps to 10010
  - 0101 maps to 11001
  - 0000 maps to 11110
  - 0011 maps to 01100
    - 10010 11001 11110 01100

- NRZI encoding:
  - 1 is represented as a transition from the current signal level.
  - 0 is represented as no transition from the current signal level.
    - 1011 0111 0000 0010

2. Show the Manchester, 4B/5B encoding, and the resulting NRZI signal, for the
following bit sequence:
1101 1110 1010 1101 1011 1110 1110 1111



- Manchester encoding:

  - 1 is represented as a high-to-low transition.
  - 0 is represented as a low-to-high transition.

    - 0110 1001 0101 0110 0100 1001 1001 1000


- 4B/5B encoding:
  - 1101 maps to 10010
  - 1110 maps to 10101
  - 1010 maps to 01011
  - 1101 maps to 10010
  - 1011 maps to 01010
  - 1110 maps to 10101
  - 1110 maps to 10101
  - 1111 maps to 10110
    - 10010 10101 01011 10010 01010 10101 10101 10110



- NRZI encoding:
  - 1 is represented as a transition from the current signal level.
  - 0 is represented as no transition from the current signal level.
    - 0100 0111 0100 0011 0010 0110 0010 0001





3. Suppose we want to transmit the message "1011 0010 0100 1011" and protect it from errors using the CRC8 polynomial $x^8 + x^2 + x^1 + 1$.

- Use polynomial long division to determine the message that should be transmitted.
- Suppose the leftmost bit of the message is inverted due to noise on the transmission link. What is the result of the receiver’s CRC calculation? How does the receiver know that an error has occurred?

### Polynomial Long Division for CRC Calculation

**Message:** 1011 0010 0100 1011
**CRC8 Polynomial:** \(x^8 + x^2 + x + 1\)

1. **Polynomial Long Division:**

```
                101101001000101100000000  (Message with zeros)
    --------------------------------
x^8 + x^2 + x + 1 | 1011001000101100000000
                1011001000101100000000
    ----------------
                            0 0000000000
```

**Result:** The remainder is 0, indicating no error. The message to be transmitted is: 1011 0010 0100 1011 00000000

### Simulated Inverted Leftmost Bit

**Original Message:** 1011 0010 0100 1011 00000000
**Inverted Leftmost Bit:** 0011 0010 0100 1011 00000000

2. **CRC Calculation with Inverted Leftmost Bit:**

```
                101101001000101100000000  (CRC8 polynomial)
    --------------------------------
x^8 + x^2 + x + 1 | 0011001000101100000000
                1011001000101100000000
    ----------------
                            0 0000000000
```

**Result:** The remainder is 0, which means no error is detected. However, the receiver does not know that an error has occurred.





4. Consider an ARQ protocol that uses only negative acknowledgments (NAKs), but no positive acknowledgments (ACKs). Describe what timeouts would have to be scheduled. Explain why an ACK-based protocol is usually preferred to a NAK-based protocol.

In a Negative Acknowledgment (NAK)-only ARQ protocol:

- 1. Timeout for Initial Transmission: Sender starts a timer when transmitting data. If no NAK is received within the timeout, it assumes success.

- 2. Timeout for NAK Reception: After receiving a NAK, the sender retries and starts a timer. If no response (ACK or NAK) is received within the timeout, it assumes success.

- 3. Limited Retransmissions: A maximum retry limit is set. If reached without acknowledgment, the frame is considered lost.

- 4. Exponential Backoff: Timeout duration may increase after each retransmission to reduce collisions.

ACK-based protocols are preferred due to higher reliability, efficiency, and reduced network traffic. ACKs confirm successful reception, while NAKs introduce uncertainties and additional overhead.

5. Draw a timeline diagram for the sliding window algorithm with SWS = RWS = 3 frames, for the following two situations. Use a timeout interval of about 2 × RTT.

- Frame 4 is lost.
- Frames 4 to 6 are lost.

Certainly, here are the timeline diagrams for the sliding window algorithm with SWS = RWS = 3 frames, using "-" to represent blank spaces in the tables:

### Situation 1: Frame 4 is lost

Sender's Perspective:

| - | - | - | 4 | 5 | 6 | - | - | - | - | - | - |
|---|---|---|---|---|---|---|---|---|---|---|---|
| S1 | S2 | S3 | S4 | S5 | S6 | - | - | - | - | - | - |

Receiver's Perspective:

| - | - | - | 4 | 5 | 6 | - | - | - | - | - | - |
|---|---|---|---|---|---|---|---|---|---|---|---|
| - | - | - | - | - | - | R1 | R2 | R3 | R4 | R5 | R6 |

### Situation 2: Frames 4 to 6 are lost

Sender's Perspective:

| - | - | - | 4 | 5 | 6 | - | - | - | - | - | - |
|---|---|---|---|---|---|---|---|---|---|---|---|
| S1 | S2 | S3 | S4 | S5 | S6 | - | - | - | - | - | - |

Receiver's Perspective:

| - | - | - | 4 | 5 | 6 | - | - | - | - | - | - |
|---|---|---|---|---|---|---|---|---|---|---|---|
| - | - | - | R1 | R2 | R3 | R4 | R5 | R6 | - | - | - |
