**Title: Functional Description**

- *CFB128 (128-bit Cipher Feedback)*

  - Interrupt on completion of computation
  
For details, see [ESP32-C3 Technical Reference Manual > Chapter AES Accelerator (AES)](#).

---

### 4.1.4.2 HMAC Accelerator

The HMAC Accelerator (HMAC) module is designed to compute Message Authentication Codes (MACs) using the SHA-256 Hash algorithm and keys as described in RFC 2104. It provides hardware support for HMAC computations, significantly reducing software complexity and improving performance.

**Feature List**
- Standard HMAC-SHA-256 algorithm
- Hash result only accessible by configurable hardware peripheral (in downstream mode)
- Compatible to challenge-response authentication algorithm
- Generates required keys for the Digital Signature (DS) peripheral (in downstream mode)
- Re-enables soft-disabled JTAG (in downstream mode)

For details, see [ESP32-C3 Technical Reference Manual > Chapter HMAC Accelerator](#).

---

### 4.1.4.3 RSA Accelerator

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly improving their run time and reducing their software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly.

**Feature List**
- Large-number modular exponentiation with two optional acceleration options, operands width up to 3072 bits
- Large-number modular multiplication, operands width up to 3072 bits
- Large-number multiplication, operands width up to 1536 bits
- Operands of different widths
- Interrupt on completion of computation

For details, see [ESP32-C3 Technical Reference Manual > Chapter RSA Accelerator](#).

---

### 4.1.4.4 SHA Accelerator

The SHA Accelerator (SHA) is a hardware device that speeds up SHA algorithm significantly, compared to SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-C3 has two working modes, which are Typical SHA and DMA-SHA.

---

**Footer:**
- Espressif Systems
- Page 43 of [ESP32-C3 Series Datasheet v2.2](#)
- Submit Documentation Feedback