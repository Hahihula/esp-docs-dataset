**Title: Functional Description**

- *CFB128 (128-bit Cipher Feedback)*

    - Interrupt on completion of computation.

For details, see [ESP32-C6 Technical Reference Manual > Chapter AES Accelerator (AES)](#).

---

### 4.1.4.2 ECC Accelerator

The ECC Accelerator accelerates calculations based on the Elliptic Curve Cryptography (ECC) algorithm and ECC-derived algorithms like ECDSSA, which offers the advantages of smaller public keys compared to RSA cryptography with equivalent security.

**Feature List**
- Supports two different elliptic curves (P-192 and P-256)
- Six working modes that supports Base Point Verification, Base Point Multiplication, Jacobian Point Verification, and Jacobian Point Multiplication

For details, see the [ESP32-C6 Technical Reference Manual > Chapter ECC Accelerator (ECC)](#).

---

### 4.1.4.3 HMAC Accelerator

The HMAC Accelerator (HMAC) module is designed to compute Message Authentication Codes (MACs) using the SHA-256 Hash algorithm and keys as described in RFC 2104. It provides hardware support for HMAC computations, significantly reducing software complexity and improving performance.

**Feature List**
- Standard HMAC-SHA-256 algorithm
- HMAC-SHA-256 calculation based on key in eFuse:
    - Whose result cannot be accessed by software in downstream mode for high security.
    - Whose result can be accessed by software in upstream mode

Generates required keys for the Digital Signature Algorithm (DSA) peripheral in downstream mode.

Re-enables soft-disabled, JTAG in downstream mode

For details, see the [ESP32-C6 Technical Reference Manual > Chapter HMAC Accelerator](#).

---

### 4.1.4.4 RSA Accelerator

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly improving their run time and reducing their software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly.

**Feature List**
- Large-number modular exponentiation with two optional acceleration options, operands width up to 3072 bits

Espressif Systems  
47  
[Submit Documentation Feedback](#)  
ESP32-C6 Series Datasheet v1.4