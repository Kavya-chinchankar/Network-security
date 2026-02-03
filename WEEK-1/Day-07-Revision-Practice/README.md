# WEEK 1 – NETWORKING FOUNDATIONS

## DAY 7 – REVISION & PRACTICE

---

This day is designed to **consolidate everything learned in Week 1**, so you can confidently **explain concepts, draw diagrams, solve subnetting problems, and answer interview questions**.

---

## 1. Draw Full Packet Flow Diagram

To visualize data flow from source to destination, always include:

* All **OSI layers**
* **Encapsulation & decapsulation**
* **Network devices** (switch, router)

### Example: Sending a Web Request

**Scenario:** Laptop → Switch → Router → Server (HTTP request)

### Layer-by-Layer Flow

**Application Layer**

* Browser sends HTTP request (`GET /index.html`)

**Presentation Layer**

* Data formatted
* Encrypted if HTTPS

**Session Layer**

* Session established (TCP handshake)

**Transport Layer (TCP)**

* Adds source & destination port numbers
* Adds sequence numbers
* Data encapsulated into segments

**Network Layer (IP)**

* Adds source and destination IP addresses
* Packet becomes routable

**Data Link Layer (Ethernet)**

* Adds source & destination MAC addresses
* Frame sent to switch

**Physical Layer**

* Bits transmitted as electrical / optical / wireless signals

### Router Forwarding Logic

* Data Link header changes at every hop
* Network layer IP addresses remain the same

### Server Receives

* Headers removed layer by layer (decapsulation)
* Original HTTP request delivered to application

**Interview Tip:**

> Always explain **encapsulation → transmission → decapsulation** while drawing the flow.

---

## 2. Subnet Practice Questions

### Practice Question 1

**Network:** `192.168.1.0/24`

**Task:** Subnet into 4 equal subnets

**Solution:**

* /24 → 256 IPs
* 4 subnets → 2 additional bits → **/26**
* Block size = 64

| Subnet | Network Address | Broadcast Address | Usable Hosts |
| ------ | --------------- | ----------------- | ------------ |
| 1      | 192.168.1.0     | 192.168.1.63      | .1 – .62     |
| 2      | 192.168.1.64    | 192.168.1.127     | .65 – .126   |
| 3      | 192.168.1.128   | 192.168.1.191     | .129 – .190  |
| 4      | 192.168.1.192   | 192.168.1.255     | .193 – .254  |

---

### Practice Question 2 (VLSM)

**Network:** `10.0.0.0/22`

| Department | Required Hosts | Subnet | Usable Hosts |
| ---------- | -------------- | ------ | ------------ |
| Dept A     | 100            | /25    | 126          |
| Dept B     | 50             | /26    | 62           |
| Dept C     | 20             | /27    | 30           |

**Rule:** Assign **largest subnet first** to avoid overlap.

---

## 3. Explain TCP Handshake (Interview Practice)

Practice saying this clearly:

> “TCP is connection-oriented. To establish a connection, it uses a 3-way handshake. First, the client sends a SYN with its initial sequence number. Second, the server responds with SYN-ACK, acknowledging the client’s sequence and sending its own. Third, the client sends an ACK, completing the handshake. After this, reliable communication begins.”

**Tip:** Use hand movements or a simple diagram to show sequence numbers.

---

## 4. Mock Interview Questions (High Probability)

### OSI & TCP/IP

* Explain OSI model with a real-life example
* Difference between TCP and UDP
* Explain flow control and congestion control

### IP & Subnetting

* Why CIDR replaced classful addressing?
* Subnet `192.168.10.0/24` for 3 departments
* Explain public vs private IP and NAT

### Protocols & Security

* HTTP vs HTTPS
* FTP vs SFTP
* What is a SYN flood attack?
* Explain DNS spoofing and mitigation

### Packet Flow

* Draw and explain full packet flow
* Explain encapsulation and decapsulation

---

## 5. Day 7 Revision Checklist

You should be able to:

* Draw a **complete packet flow diagram**
* Solve **classful and VLSM subnetting** quickly
* Explain **TCP handshake confidently**
* Compare protocols clearly
* Explain **common attacks and mitigations**
* Use **real-life analogies** while explaining

---

### Final Interview Tip

Speak slowly, structure answers, draw diagrams where possible, and **always relate networking concepts to security when applicable**.
