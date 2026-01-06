# WEEK 1 – NETWORKING FOUNDATIONS  
## DAY 5 – TCP vs UDP (Transport Layer)

This module provides a **beginner-to-interview-level explanation of TCP and UDP**, focusing on **core concepts, internal mechanisms, real-world usage, and security relevance**.  
By the end of this day, you should be able to **explain TCP vs UDP confidently in interviews**, including handshake, flow control, congestion control, and common attacks.

---

## 1. TCP vs UDP – Core Comparison

TCP and UDP operate at the **Transport Layer (OSI Layer 4)** and manage **end-to-end communication** between applications.

| Feature            | TCP                         | UDP                     |
|--------------------|-----------------------------|--------------------------|
| Type               | Connection-oriented         | Connectionless           |
| Reliability        | Reliable                    | Unreliable               |
| Error Detection    | ACKs & retransmissions      | Checksum only            |
| Packet Ordering    | Guaranteed                  | Not guaranteed           |
| Flow Control       | Yes                         | No                       |
| Congestion Control | Yes                         | No                       |
| Speed              | Slower                      | Faster                   |
| Use Cases          | Web, Email, File Transfer   | Streaming, DNS, VoIP     |

**Key Concept:**
- **TCP** prioritizes reliability and correctness  
- **UDP** prioritizes speed and low latency

---

## 2. TCP 3-Way Handshake (Connection Establishment)

TCP establishes a connection before data transmission using a **3-way handshake**.

### Steps

1. **SYN**
   - Client sends a SYN packet with an initial sequence number

2. **SYN-ACK**
   - Server responds with SYN + ACK
   - Acknowledges client sequence number
   - Sends its own sequence number

3. **ACK**
   - Client acknowledges the server sequence number
   - Connection is established

**Interview Line:**
> “TCP establishes a reliable connection using a three-way handshake: SYN, SYN-ACK, and ACK.”

---

## 3. Flow Control (Sliding Window)

**Problem:**  
The sender may send data faster than the receiver can process.

**TCP Solution:**  
- Receiver advertises a **window size**
- Sender limits data transmission based on this window

**Analogy:**  
Water flow controlled by a valve to avoid overflow.

**Interview Line:**
> “TCP flow control uses a sliding window to prevent the sender from overwhelming the receiver.”

---

## 4. Congestion Control

**Problem:**  
Excessive packets in the network can cause congestion and packet loss.

**TCP Mechanisms:**
1. Slow Start  
2. Congestion Avoidance  
3. Fast Retransmit  
4. Fast Recovery  

**Interview Line:**
> “TCP congestion control prevents network overload using slow start and congestion avoidance algorithms.”

---

## 5. Ports and Sockets

### Ports
- Identify specific applications on a host
- Range: **0–65535**

| Range        | Description         | Example        |
|--------------|---------------------|----------------|
| 0–1023       | Well-known ports    | HTTP (80)      |
| 1024–49151   | Registered ports    | App services   |
| 49152–65535  | Dynamic/Private     | Client ports   |

### Sockets
A socket uniquely identifies a connection using:
- IP Address
- Port Number
- Protocol (TCP/UDP)

**Example:**  
`192.168.1.10:443/TCP`

**Interview Line:**
> “A socket is a combination of IP address, port, and protocol.”

---

## 6. UDP – Key Characteristics

- No connection setup
- No acknowledgments
- No retransmission
- Minimal overhead

**Use Cases:**
- Live streaming
- Video calls
- DNS queries
- Online gaming

**Analogy:**
> “UDP is like sending a postcard — fast, but no delivery guarantee.”

---

## 7. Security Focus – SYN Flood Attack

### How SYN Flood Works

1. Attacker sends大量 SYN requests
2. Server allocates resources for half-open connections
3. Attacker never sends final ACK
4. Server resources get exhausted

**Impact:**  
Denial of Service (DoS)

### Mitigation
- SYN cookies
- Firewall rate limiting
- Intrusion Detection/Prevention Systems

**Interview Line:**
> “A SYN flood attack exploits TCP’s handshake by creating multiple half-open connections.”

---

## 8. Real-Life Examples

- **TCP:** Sending an email (accuracy matters)
- **UDP:** Live sports streaming (speed matters)

---

## 9. Day 5 Revision Checklist

You should be able to:
- Clearly compare TCP and UDP
- Explain the 3-way handshake
- Describe flow control and congestion control
- Explain ports and sockets
- Describe SYN flood attacks and mitigation
- Provide real-world examples

---

### Next Topic
➡️ **Day 6 – Common Protocols (HTTP, HTTPS, FTP, SMTP, DNS, Security Attacks)**

This day builds on TCP/UDP concepts and introduces **application-layer protocols with security relevance**.
