**Title: Functional Description**

---

### **4.1.3.14 Debug Assistant**

The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

#### Feature List

- Read/write monitoring: Monitor whether the CPU bus reads from or writes to a specified memory address space
- Stack pointer (SP) monitoring: Prevent stack overflow or erroneous push/pop operations violation will trigger an interrupt.
- Program counter (PC) logging: Record PC value. The developer can get the last PC value at the most recent CPU reset
- Bus access logging: Record information about bus access when the CPU or DMA writes a specified value

---

### **4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

#### 4.1.4.1 ECC Accelerator

The ECC Accelerator accelerates calculations based on the Elliptic Curve Cryptography (ECC) algorithm and ECC-derived algorithms like ECDSA, which offers the advantages of smaller public keys compared to RSA cryptography with equivalent security.

#### Feature List

- Supports two different elliptic curves (P-192 and P-256)
- 11 working modes that supports Base Point Verification, Base Point Multiplication, Jacobian Point Verification, and Jacobian Point Multiplication
- Secure operating mode for Base Point Multiplication in a fixed amount of time

#### **4.1.4.2 Elliptic Curve Digital Signature Algorithm (ECDSA)**

In cryptography, the Elliptic Curve Digital Signature Algorithm (ECDSA) offers a variant of the Digital Signature Algorithm (DSA) which uses elliptic-curve cryptography.

ESP32-C61’s ECDSA accelerator provides a secure and efficient environment for computing ECDSA signatures. It offers fast computations while ensuring the confidentiality of the signing process to prevent information leakage. This makes it a valuable tool for applications that require high-speed cryptographic operations with strong security guarantees. By using the ECDSA accelerator, users can be confident that their data is being protected without sacrificing performance.

---

**Footer:**
Espressif Systems
41 ESP32-C61 Series Datasheet v0.5