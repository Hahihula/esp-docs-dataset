**Title: Functional Description**

- *CFB8 (8-bit Cipher Feedback)*
- *CFB128 (128-bit Cipher Feedback)*

For details, see [ESP32-C5 Technical Reference Manual > Chapter AES Accelerator (AES)](#).

---

### 4.1.4.2 ECC Accelerator

Elliptic Curve Cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves. ECC allows smaller keys compared to RSA cryptography while providing equivalent security.

ESP32-C5’s ECC Accelerator can complete various calculations based on different elliptic curves, thus accelerating the ECC algorithm and ECC-derived algorithms such as ECDSA).

**Feature List**
- three elliptic curves, namely P-192, P-256 and P-384 defined in [FIPS 186-3](#)
- two coordinate systems, namely Affine Coordinates and Jacobian Coordinates
- different point operations, including point addition, point multiplication, and point verification
- different modular operations based on the order or mod base of the curve, including mod addition, mod subtraction, mod multiplication, and mod division
- interrupt upon completion of calculation
- secure operating mode for Base Point Multiplication within a specified time frame

For details, see [ESP32-C5 Technical Reference Manual > Chapter ECC Accelerator (ECC)](#).

---

### 4.1.4.3 HMAC Accelerator

The HMAC Accelerator (HMAC) module is designed to compute Message Authentication Codes (MACs) using the SHA-256 Hash algorithm and keys as described in RFC 2104. It provides hardware support for HMAC computations, significantly reducing software complexity and improving performance.

**Feature List**
- standard HMAC-SHA-256 algorithm
- hash result only accessible by configurable hardware peripheral (in downstream mode)
- compatibility with challenge-response authentication algorithm
- required keys for the Digital Signature (DS) peripheral in downstream mode
- re-enabled soft-disabled JTAG (in downstream mode)

For details, see [ESP32-C5 Technical Reference Manual > Chapter HMAC Accelerator](#).

---

**Footer:**
Espressif Systems  
45  
[Submit Documentation Feedback](#)  
ESP32-C5 Series Datasheet v1.0