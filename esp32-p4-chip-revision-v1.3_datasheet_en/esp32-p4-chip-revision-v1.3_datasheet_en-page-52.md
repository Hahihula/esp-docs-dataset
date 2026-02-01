**4 Functional Description**

- GCM (Galois/Counter Mode)
- Interrupt on completion of computation

---

**4.1.5.2 ECC Accelerator (ECC)**

Elliptic Curve Cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves. ECC allows smaller keys compared to RSA cryptography while providing equivalent security.

ESP32-P4’s ECC accelerator can complete various calculations based on different elliptic curves, thus accelerating the ECC algorithm and ECC-derived algorithms (such as ECDSA).

**Feature List**
- 2 different elliptic curves, namely P-192 and P-256 defined in [FIPS 186-3](https://www.nist.gov/pubs/detail/fips/fips186-3)
- 11 working modes
- Interrupt upon completion of calculation

---

**4.1.5.3 HMAC Accelerator (HMAC)**

The Hash-based Message Authentication Code (HMAC) module computes Message Authentication Codes (MACs) using hash algorithm SHA-256 and keys as described in RFC 2104. The 256-bit HMAC key is stored in an eFuse key block and can be set as read-protected, i.e., the key is not accessible from outside the HMAC accelerator.

**Feature List**
- Standard HMAC-SHA-256 algorithm
- HMAC-SHA-256 calculation based on key in eFuse,
  - whose result cannot be accessed by software in downstream mode for high security
  - whose result can be accessed by software in upstream mode

Generates required keys for the Digital Signature Algorithm (DSA) peripheral in downstream mode.

Re-enables soft-disabled JTAG in downstream mode

---

**4.1.5.4 RSA Accelerator (RSA)**

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly reducing the operation time and software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator speeds up RSA algorithms significantly. The RSA accelerator also supports operands of different lengths, which provides more flexibility during the computation.

**Feature List**
- Large-number modular exponentiation with two optional acceleration options

---

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-P4 Series Datasheet v0.6