# WEEK 1 – NETWORKING FOUNDATIONS

## DAY 6 – COMMON PROTOCOLS

---

## 1. Why Protocols Are Important

- Protocols define how devices communicate
- They specify:
  - Data format
  - Communication rules
  - Error handling

**Analogy:**
- Protocols are like languages (English, French, etc.)

---

## 2. HTTP vs HTTPS

### HTTP – Hypertext Transfer Protocol
- Layer: Application (OSI Layer 7)
- Port: 80
- Stateless protocol
- Data sent in plain text (insecure)

**Working:**
1. Client sends HTTP request
2. Server responds with resource

---

### HTTPS – Secure HTTP
- Port: 443
- Uses TLS/SSL encryption
- Ensures confidentiality and integrity

**Benefits:**
- Prevents packet sniffing
- Verifies server identity
- Protects against MITM attacks

**Interview Line:**

> “HTTPS secures HTTP traffic using TLS/SSL encryption to ensure confidentiality and integrity.”

---

## 3. FTP vs SFTP

### FTP – File Transfer Protocol
- Port: 21 (control), 20 (data)
- Unencrypted
- Credentials sent in plain text

**Interview Line:**

> “FTP is insecure because data and credentials are transmitted in plain text.”

---

### SFTP – Secure File Transfer Protocol
- Port: 22
- Uses SSH encryption
- Secure authentication and data transfer

**Interview Line:**

> “SFTP transfers files securely using SSH encryption.”

---

## 4. Email Protocols

### SMTP – Simple Mail Transfer Protocol
- Port: 25 / 587
- Used for sending emails
- Works client → server or server → server

---

### POP3 – Post Office Protocol v3
- Port: 110
- Downloads emails to local system
- Emails usually deleted from server

---

### IMAP – Internet Message Access Protocol
- Port: 143 / 993
- Emails remain on server
- Sync across multiple devices

**Interview Line:**

> “SMTP sends emails, POP3 downloads emails, and IMAP allows synchronized access.”

---

## 5. DNS – Domain Name System

- Converts domain names to IP addresses
- Example: www.google.com → IP address

### DNS Lookup Steps
1. Local cache check
2. Recursive resolver
3. Root server
4. TLD server
5. Authoritative server

**Interview Line:**

> “DNS resolves domain names into IP addresses for proper routing.”

---

## 6. Security – DNS Spoofing

- Attacker injects fake DNS records
- Redirects users to malicious sites
- Used for credential theft

### Mitigation
- DNSSEC
- Trusted DNS resolvers
- DNS log monitoring

**Interview Line:**

> “DNS spoofing redirects users using fake DNS records and can be mitigated with DNSSEC.”

---

## 7. Common Protocols – Quick Reference

| Protocol | Purpose              | Port    | Security                  |
|---------|----------------------|---------|---------------------------|
| HTTP    | Web browsing         | 80      | Plain text                |
| HTTPS   | Secure web           | 443     | TLS/SSL                   |
| FTP     | File transfer        | 21      | Plain text                |
| SFTP    | Secure file transfer | 22      | SSH encryption            |
| SMTP    | Send email           | 25/587  | TLS supported             |
| POP3    | Download email       | 110     | SSL supported             |
| IMAP    | Access email         | 143/993 | SSL/TLS                   |
| DNS     | Name resolution      | 53      | Vulnerable without DNSSEC |

---

## 8. Real-Life Analogies

- HTTP/HTTPS → Sending letters online
- FTP/SFTP → Moving files between computers
- SMTP → Mailman sending letters
- POP3 → Collecting letters from mailbox
- IMAP → Reading letters without removing them
- DNS → Phone book mapping names to numbers

---

## 9. Day 6 – Revision Checklist

You should be able to:
1. Explain HTTP vs HTTPS
2. Explain FTP vs SFTP
3. Explain SMTP, POP3, IMAP
4. Explain DNS lookup process
5. Explain DNS spoofing and mitigation
6. Use real-life analogies
