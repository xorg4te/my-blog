---
title: TCP Sessions
date: 2024-07-30 11:35:00 +0800
categories: [other]
tags: [networking]     # TAG names should always be lowercase
---

**Hello !** Hope you're well. For our first post, we're going to cover some very important concepts. The [TCP protocol](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) is now used everywhere for data transfer. In this post, we'll look at how a [TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) session is established and what it's used for in most cases. 

---

![herewego](/assets/img/IMG_2648.gif)

---

# Understanding TCP Sessions

[TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) sessions are the backbone of reliable communication on the Internet. Whether you’re **streaming videos**, **sending emails**, or **browsing the web**, [TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) ensures your data gets to its destination accurately. 

![datatransfer](/assets/img/IMG_2662.gif)

Let's dive into the details of this essential [protocol](https://www.cloudflare.com/en-gb/learning/network-layer/what-is-a-protocol/).

## Why is TCP Important ?

[TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol), or Transmission Control Protocol, ensures **reliable** and **orderly** data transmission between two computers. Unlike other protocols such as [UDP](https://en.m.wikipedia.org/wiki/User_Datagram_Protocol) ( User Datagram Protocol ), [TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) guarantees that **every packet** of data sent arrives at its destination and in the **correct order**. This is crucial for applications where data loss is unacceptable, like **file downloads** or **web browsing**.

## How Does a TCP Session Work ?

### Establishing the Connection: The Three-Way Handshake

To start a [TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) session, the two computers must first establish a connection. This process, known as the **three-way handshake**, involves three steps :

![handshake](/assets/img/IMG_2664.gif)

1. **SYN ( Synchronize )** : Computer A sends a SYN segment to Computer B to initiate the connection.
2. **SYN-ACK ( Synchronize-Acknowledge )** : Computer B responds with a SYN-ACK segment, acknowledging the SYN and requesting synchronization.
3. **ACK (Acknowledge)** : Computer A sends an ACK segment to acknowledge the SYN-ACK from Computer B. The connection is now established.

### Data Transfer

Once the connection is **established**, data can be exchanged reliably. Each data packet sent is accompanied by a **unique sequence number**, allowing the receiving computer to reconstruct the data in the correct order.

### Flow Control and Congestion Control

[TCP](https://en.m.wikipedia.org/wiki/Transmission_Control_Protocol) uses flow control and congestion control mechanisms to optimize data transfer :

- **Receive Window** : The receiver indicates how much data it can receive before it must send an acknowledgment.
- **Congestion Control Algorithm** : TCP dynamically adjusts the data transmission rate to avoid network congestion.

### Closing the Connection

When the communication is complete, the two computers must close the connection in an orderly manner. This process uses another set of messages :



1. **FIN (Finish)** : Computer A sends a FIN segment to indicate it has finished sending data.
2. **ACK** : Computer B acknowledges the FIN with an ACK segment.
3. **FIN** : Computer B then sends its own FIN segment.
4. **ACK** : Finally, Computer A acknowledges this FIN with an ACK segment, and the connection is terminated.

## Advantages and Limitations of TCP

### Advantages
- **Reliability**: Ensures correct data delivery.
- **Error Control**: Uses mechanisms to detect and correct transmission errors.
- **Order**: Maintains the order of data packets.

### Limitations
- **Overhead**: Control and acknowledgment mechanisms add extra overhead.
- **Latency**: The connection-oriented nature and control processes can introduce some latency.

## Conclusion

TCP is a robust and reliable protocol that plays a crucial role in modern Internet communications. By understanding how TCP sessions work, you can better appreciate the challenges and solutions related to data transmission over networks. Next time you download a file or stream a video, remember that TCP is working behind the scenes to ensure everything runs smoothly.
