# Cyber Squad - Day 3: Cryptography and Network Traffic Analysis

**Platform:** U.S. Cyber Range Exercise Area (Linux environment with Wireshark).
**Duration:** about 4 hours.

---

## Learning objectives
- Distinguish encoding, encryption, and hashing.
- Capture and read network packets with Wireshark inside the range.
- See the difference between unencrypted (HTTP) and encrypted (HTTPS) traffic.

## Vocabulary (acronyms expanded and defined)
- **Encoding / Encryption / Hashing**: reformat / scramble with a key / one-way fingerprint.
- **AES = Advanced Encryption Standard**; **RSA = Rivest-Shamir-Adleman**.
- **Wireshark**: a tool that captures and displays network packets.
- **Packet**: a small chunk of data sent across a network.
- **HTTP = HyperText Transfer Protocol**; **HTTPS = HTTP Secure**.
- **TLS = Transport Layer Security**: the encryption behind HTTPS.

## Instructor setup
1. Launch a U.S. Cyber Range environment that includes Wireshark and two communicating hosts inside the isolated network.
2. Prepare a short demonstration of capturing traffic between the in-range hosts. All traffic stays inside the range.
3. Review classic-cipher concepts from Course 6302 so students connect math to real protocols.

## Student lab
1. Classic ciphers warm-up (notebook): encrypt and brute-force a Caesar cipher, then XOR a message and recover it.
2. Capture packets in Wireshark:
   - Start a capture on the lab interface.
   - Generate some traffic between the in-range hosts as directed.
   - Stop the capture and apply a display filter such as `http` or `tcp`.
3. Compare: find a plain HTTP exchange and note that text is readable. Then look at an HTTPS exchange and note that the contents are encrypted by TLS.

## Mini-lesson
```
  HTTP  : Browser ---- readable text ----> Server     (anyone sniffing can read it)
  HTTPS : Browser ==== encrypted (TLS) ===> Server    (a sniffer sees only scrambled bytes)
```

## In the news (real and verifiable)
The shift of the web to HTTPS by default, encouraged by browsers and free certificate programs, made packet sniffing far less useful to attackers on shared networks. During World War Two, breaking the Enigma cipher at Bletchley Park showed how decisive cryptography can be, a lesson still central to security today.

## Assessment
- Numerical: a Caesar cipher has how many useful shift keys? (Answer: 25.)
- MCQ: HTTPS protects traffic using a) ROT13 b) TLS encryption c) Base64. (Answer: b.)
- Practical check: student shows one HTTP packet with readable text and explains why HTTPS would hide it.

## Coding
Open **Day3.ipynb** for the cipher and XOR exercises.
