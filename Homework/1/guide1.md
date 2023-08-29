# Study Guide: Chapter 1 - Computer Networks: A Systems Approach

## Introduction
Welcome to the study guide for Chapter 1 of the textbook "Computer Networks: A Systems Approach" by Larry Peterson and Bruce Davie. This guide will help you understand the fundamental concepts of computer networks and provide you with questions and exercises to reinforce your understanding. Let's get started!

### Required reading
Sections: 1.1, 1.2, 1.3 and 1.5 

## 1. Building a Scalable Network
- What are the key considerations when building a scalable network?
  When building a scalable network, there are several key considerations to keep in mind. These considerations include:

  1. Network Architecture: Designing a scalable network requires a well-thought-out architecture that can accommodate future growth and expansion. This involves considering factors such as network topology, routing protocols, and network segmentation.
   
  2. Bandwidth: Sufficient bandwidth is crucial for a scalable network. It is important to assess the current and future bandwidth requirements of the network and ensure that the network infrastructure can handle the expected traffic volume.
   
  3. Redundancy: Building redundancy into the network is essential for ensuring high availability and minimizing downtime. This can be achieved through redundant network links, redundant hardware components, and implementing failover mechanisms.
   
  5. Security: Implementing robust security measures is crucial for protecting the network from potential threats. This includes using firewalls, intrusion detection systems, and encryption protocols to safeguard network traffic and data.
   
  6. Network Monitoring and Management: Having effective network monitoring and management tools in place is essential for identifying and resolving issues promptly. This includes monitoring network performance, analyzing traffic patterns, and proactively managing network resources.
   
  7. Future Growth: Anticipating future growth and planning for scalability is vital. This involves considering factors such as the number of users, devices, and applications that the network will need to support in the future.

- Explain the concept of network scalability and why it is important.

Network scalability refers to the ability of a computer network to accommodate an increasing number of users, devices, and data traffic without experiencing a significant decrease in performance or functionality. It is important in building a computer network from scratch because it allows the network to grow and adapt to the changing needs of an organization or business.

When building a computer network from scratch, it is crucial to consider scalability to ensure that the network can handle future growth and expansion. Without scalability, the network may become overloaded and unable to handle the increased demands placed on it. This can result in slow performance, network congestion, and even network failures.

Scalability also allows for flexibility in adding new devices, applications, and services to the network. It enables the network to easily accommodate new users and devices without requiring significant changes or disruptions to the existing infrastructure. This is particularly important in today's rapidly evolving technological landscape, where new devices and technologies are constantly being introduced.

In summary, network scalability is important in building a computer network from scratch because it ensures that the network can handle future growth, adapt to changing needs, and provide optimal performance and functionality.

- Provide examples of different applications that require a scalable network.
  Some examples of applications that require a scalable network include:

  1. Cloud computing: Cloud service providers need a scalable network infrastructure to handle the increasing demand for storage, processing power, and data transfer.
    
  2. E-commerce platforms: Online shopping websites experience high traffic during peak times, such as holidays or sales events. A scalable network is necessary to handle the increased number of users and transactions.
    
  3. Social media platforms: Social networking sites like Facebook, Twitter, and Instagram have millions of active users who generate and consume large amounts of data. A scalable network is essential to handle the constant flow of information.
    
  4. Video streaming services: Platforms like Netflix, YouTube, and Hulu require a scalable network to deliver high-quality video content to a large number of users simultaneously.
    
  5. Online gaming: Multiplayer online games require a scalable network to support real-time communication and interaction between players.
    
  6. Big data analytics: Applications that process and analyze massive amounts of data, such as data mining, machine learning, and artificial intelligence, require a scalable network to handle the computational and storage requirements.
    
  7. Internet of Things (IoT): IoT devices, such as smart home devices, wearables, and industrial sensors, generate a vast amount of data that needs to be transmitted and processed. A scalable network is necessary to handle the increasing number of connected devices.

- Why does a network need to be cost-effective, fair, and have robust connectivity?

  1. Cost-effectiveness: A cost-effective network ensures that the resources and infrastructure required to establish and maintain the network are optimized. This includes minimizing the expenses associated with hardware, software, maintenance, and operational costs. By being cost-effective, a network can provide services and connectivity at an affordable price, making it accessible to a wider range of users.
    
  2. Fairness: Fairness in a network refers to the equitable distribution of network resources among users. It ensures that all users have equal opportunities to access and utilize network services without any discrimination or bias. Fairness prevents any single user or group from monopolizing network resources, leading to a more balanced and inclusive network environment.
    
  3. Robust connectivity: Robust connectivity is crucial for a network to ensure reliable and uninterrupted communication. A network with robust connectivity can handle high volumes of traffic, provide low latency, and maintain consistent performance even during peak usage periods. It minimizes downtime, packet loss, and other disruptions, thereby enhancing user experience and productivity.


- Discuss the challenges involved in designing a network that can support various applications.

  1. Bandwidth requirements: Different applications have different bandwidth requirements. Some applications, such as video streaming or online gaming, require high bandwidth to function properly. Designing a network that can allocate sufficient bandwidth to each application can be a challenge.
    
  2. Quality of Service (QoS): Certain applications, like voice or video conferencing, require low latency and high priority to ensure a smooth user experience. Designing a network that can prioritize traffic and provide the necessary QoS for different applications can be complex.
    
  3. Scalability: As the number of applications and users on the network increases, the network should be able to scale accordingly. Designing a network that can handle the growing demands of various applications without compromising performance or stability can be a challenge.
    
  4. Security: Different applications may have different security requirements. Designing a network that can provide the necessary security measures, such as firewalls, intrusion detection systems, or encryption, for each application can be a complex task.
    
  5. Compatibility: Various applications may have different protocols or communication requirements. Designing a network that can support different protocols and ensure compatibility between applications can be challenging.


## 2. Computer Network Architecture
- Define computer network architecture in terms of layers and protocols
  Computer network architecture refers to the design and structure of a computer network. It involves the organization of the network into different layers, each providing a specific level of service. Layering helps manage the complexity of the network and allows for modular design and implementation.

Protocols are an essential part of network architecture. They define the rules and formats for communication between different components of the network. Each layer in the network architecture has its own set of protocols that provide services to higher layers and use services from lower layers.

The most widely referenced network architectures are the OSI (Open Systems Interconnection) model and the Internet architecture. The OSI model consists of seven layers, each responsible for a specific aspect of network communication. The Internet architecture, on the other hand, follows a simpler stack, with layers such as network protocols, Internet Protocol (IP), Transmission Control Protocol (TCP), User Datagram Protocol (UDP), and application protocols like HTTP, FTP, Telnet, and SMTP.

- Why are layers and protocols important?
  Layers and protocols are important in computer network architecture for several reasons:

  1. Decomposition of the problem: Layering allows the complex task of building a network to be divided into smaller, more manageable components. Each layer focuses on solving a specific part of the problem, making the overall design more modular and easier to understand.
    
  2. Abstraction: Layers provide a way to abstract away the complexity of the underlying hardware and network topology. Each layer builds on the services provided by the lower layers, providing a higher level of abstraction to the higher layers. This allows applications and protocols to interact with the network without needing to understand the details of the underlying infrastructure.
    
  3. Modularity: Layering promotes modularity in network design. If a new service or functionality needs to be added, it can often be done by modifying or adding functionality at a specific layer, without affecting the other layers. This makes it easier to update and extend the network architecture as new technologies and requirements emerge.
    
  4. Interoperability: Protocols define the rules and formats for communication between different components of the network. By adhering to a common set of protocols, different devices and systems can communicate and interoperate with each other, regardless of their specific implementations. This promotes compatibility and allows for the development of a wide range of applications and services that can work together seamlessly.

- What is encapsulation, multiplexing and demultiplexing?
  Encapsulation, multiplexing, and demultiplexing are important concepts in computer network architecture.

Encapsulation refers to the process of adding headers or trailers to a message at each layer of the protocol stack as it travels from the source to the destination. Each layer adds its own header or trailer to the message, which contains control information specific to that layer. This allows the message to be properly handled and interpreted by the corresponding layer at the destination. The headers or trailers are like envelopes that contain the message and the necessary information for its delivery.

Multiplexing is the technique of combining multiple data streams into a single stream for transmission over a shared medium or link. In the context of computer networks, multiplexing allows multiple applications or protocols to share the same network connection. Each data stream is assigned a unique identifier, known as a multiplexing key or demux key, which is included in the header of the message. This key is used by the receiving end to demultiplex the incoming messages and deliver them to the appropriate application or protocol.

Demultiplexing is the reverse process of multiplexing. It involves extracting the individual data streams from a multiplexed stream at the receiving end. The demultiplexing key in the header of the message is used to determine the destination application or protocol for each data stream. The demultiplexing process ensures that each data stream is correctly delivered to its intended recipient.

- Discuss the role of each layer in the OSI and Internet protocol stack.
  In the OSI model, each layer has a specific role:

  1. Physical Layer: This layer is responsible for the transmission of raw bits over a communication link.
    
  2. Data Link Layer: The data link layer collects a stream of bits into larger aggregates called frames. It handles the framing, error detection, and flow control.
    
  3. Network Layer: The network layer handles routing among nodes within a packet-switched network. It deals with the logical addressing and routing of packets.
    
  4. Transport Layer: The transport layer provides end-to-end communication between processes on different hosts. It ensures reliable and ordered delivery of messages.
    
  5. Session Layer: The session layer manages the communication sessions between applications. It establishes, maintains, and terminates connections between applications.
    
  6. Presentation Layer: The presentation layer is concerned with the format of data exchanged between peers. It handles data encryption, compression, and conversion.
    
  7. Application Layer: The application layer provides services directly to the end-user applications. It includes protocols like HTTP, FTP, Telnet, and SMTP.

**In the Internet protocol stack:**

1. Network Interface Layer: This layer corresponds to the physical and data link layers in the OSI model. It handles the transmission of bits over the physical medium.
2. Internet Layer: The internet layer corresponds to the network layer in the OSI model. It is responsible for logical addressing and routing of packets across different networks.
3. Transport Layer: The transport layer provides end-to-end communication between processes. It includes protocols like TCP and UDP.
4. Application Layer: The application layer includes various
   protocols that directly interact with the applications. It provides a platform-independent interface between the application and the network services.

- Provide examples of protocols used at each layer of the TCP/IP protocol stack.
  Yes, I can provide examples of protocols used at each layer of the TCP/IP protocol stack:

  1. Network Interface Layer (also known as Link Layer):
          - Ethernet
          - Wi-Fi (802.11)
          - Point-to-Point Protocol (PPP)
    
  2. Internet Layer:
          - Internet Protocol (IP)
          - Internet Control Message Protocol (ICMP)
          - Address Resolution Protocol (ARP)
    
  3. Transport Layer:
          - Transmission Control Protocol (TCP)
          - User Datagram Protocol (UDP)
    
  4. Application Layer:
          - Hypertext Transfer Protocol (HTTP)
          - File Transfer Protocol (FTP)
          - Simple Mail Transfer Protocol (SMTP)
          - Domain Name System (DNS)


## 3. Performance
- Why is important to keep track of the performance of a network?
- What are the main metrics we use to measure network performance?
- Give some examples of the challenges of using different metrics in high speed networks


## Exercises
1. Calculate the total time required to transfer a 1000-KB file in the following cases, assuming an RTT of 50 ms, a packet size of 1 KB data, and an initial 2 × RTT of “handshaking” before data is sent:

    a. The bandwidth is 1.5 Mbps, and data packets can be sent continuously.

    b. The bandwidth is 1.5 Mbps, but after we finish sending each data packet we must wait one RTT before sending the next.
    
    c. The bandwidth is “infinite,” meaning that we take transmit time to be zero, and up to 20 packets can be sent per RTT.
    
    d. The bandwidth is infinite, and during the first RTT we cansend one packet ($2^{1−1}$), during the second RTT we can send two packets ($2^{2−1}$), during the third we can send four ($2^{3−1}$), and so on
    
2. For each of the following operations on a remote file server, discuss whether they are more likely to be delay sensitive or bandwidth sensitive:

    a. Open a file.

    b. Read the contents of a file.
    
    c. List the contents of a directory.
    
    d. Display the attributes of a file.
    
3. Suppose a host has a 1-MB file that is to be sent to another host. The file takes 1 second of CPU time to compress 50% or 2 seconds to compress 60%.

    a. Calculate the bandwidth at which each compression option takes the same total compression + transmission time.
    
    b. Explain why latency does not affect your answer

4. . Discuss the relative performance needs of the following applications in terms of average bandwidth, peak bandwidth, latency, jitter, and loss tolerance:
    
    a. File server.
    
    b. Print server.
    
    c. Digital library.
    
    d. Routine monitoring of remote weather instruments.
    
    e. Voice.
    
    f. Video monitoring of a waiting room.
    
    g. Television broadcasting.


**RESOLVED**

### Exercise 1

**a. Bandwidth: 1.5 Mbps**

Transfer Time = Data Size / Bandwidth
Transfer Time = 1000 KB / (1.5 Mbps / 8 bits per byte)
Transfer Time = 6666.67 ms

Total Time = Transfer Time + 2 * RTT
Total Time = 6666.67 ms + 2 * 50 ms
Total Time = 6766.67 ms

**b. Bandwidth: 1.5 Mbps with 1 RTT wait**

Transfer Time = Data Size / Bandwidth
Transfer Time = 1000 KB / (1.5 Mbps / 8 bits per byte)
Transfer Time = 6666.67 ms

Total Time = Transfer Time + 3 * RTT (2 RTT handshaking + 1 RTT wait)
Total Time = 6666.67 ms + 3 * 50 ms
Total Time = 6816.67 ms

**c. Infinite Bandwidth (Up to 20 packets per RTT)**

Transfer Time = Data Size / (Packet Size * Number of Packets per RTT)
Transfer Time = 1000 KB / (1 KB * 20)
Transfer Time = 50 ms

Total Time = Transfer Time + 2 * RTT
Total Time = 50 ms + 2 * 50 ms
Total Time = 150 ms

**d. Infinite Bandwidth with Exponential Increase in Packets**

This is a geometric series, and the sum of such a series can be calculated as: Total Time = a * (1 - r^n) / (1 - r), where a is the initial term (1 RTT), r is the common ratio (2), and n is the number of terms.

Total Time = 1 * (1 - 2^n) / (1 - 2)
Total Time = (1 - 2^n) / -1
When n = 4 (4 RTTs), Total Time = (1 - 16) / -1 = 15 RTTs * 50 ms/RTT = 750 ms

### Exercise 2

a. Open a file: This operation is more likely to be delay sensitive. The user usually expects a quick response when requesting to open a file.

b. Read the contents of a file: This operation can be both delay and bandwidth sensitive, depending on the size of the file. Reading small files might be more delay sensitive, while reading large files could be more bandwidth sensitive.

c. List the contents of a directory: This operation is typically more delay sensitive as users expect quick responses when browsing directories.

d. Display the attributes of a file: This operation is more likely to be delay sensitive, as users would like to see file attributes quickly after requesting them.

### Exercise 3

a. To find the bandwidth at which each compression option takes the same total compression + transmission time, we need to equate the time taken for both options.

For 50% compression:
Total Time = Compression Time + Transfer Time
Total Time = 1 second (Compression Time) + 1000 KB / (Bandwidth) + 2 * RTT

For 60% compression:
Total Time = Compression Time + Transfer Time
Total Time = 2 seconds (Compression Time) + 1000 KB / (Bandwidth) + 2 * RTT

Setting the two Total Time equations equal to each other and solving for Bandwidth:
1 + 1000 / B + 2 * RTT = 2 + 1000 / B + 2 * RTT
1 = 2

This is not possible, so there's no bandwidth at which both options take the same total time.

b. Latency does not affect the answer because the latency components (compression time, transmission time, and RTT) are the same for both compression options in the equation. Changing the latency would affect the overall time, but it would affect both options equally.

### Exercise 4

a. File Server:
- Average Bandwidth: Moderate
- Peak Bandwidth: Moderate to High (during heavy file transfers)
- Latency: Relatively low
- Jitter: Low
- Loss Tolerance: Low

b. Print Server:
- Average Bandwidth: Low to Moderate
- Peak Bandwidth: Low to Moderate (during print jobs)
- Latency: Relatively low
- Jitter: Low
- Loss Tolerance: Low

c. Digital Library:
- Average Bandwidth: Moderate to High (depends on user activity)
- Peak Bandwidth: High (during periods of high usage)
- Latency: Moderate
- Jitter: Moderate
- Loss Tolerance: Low

d. Routine Monitoring of Remote Weather Instruments:
- Average Bandwidth: Low to Moderate
- Peak Bandwidth: Low to Moderate (data updates)
- Latency: Low to Moderate
- Jitter: Low
- Loss Tolerance: Moderate

e. Voice:
- Average Bandwidth: Low
- Peak Bandwidth: Low
- Latency: Very low
- Jitter: Low to Moderate
- Loss Tolerance: Low

f. Video Monitoring of a Waiting Room:
- Average Bandwidth: Moderate to High (depends on video quality)
- Peak Bandwidth: High (during live streaming)
- Latency: Low to Moderate
- Jitter: Moderate
- Loss Tolerance: Moderate

g. Television Broadcasting:
- Average Bandwidth: High
- Peak Bandwidth: Very High (during live events)
- Latency: Low to Moderate
- Jitter: Low to Moderate
- Loss Tolerance: Low




```python

```
