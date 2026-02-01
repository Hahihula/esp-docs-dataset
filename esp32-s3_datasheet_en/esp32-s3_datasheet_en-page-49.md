**Title: Functional Description**

- CBC (Cipher Block Chaining)
- OFB (Output Feedback)
- CTR (Counter)
- CFB8 (8-bit Cipher Feedback)
- CFB128 (128-bit Cipher Feedback)

Interrupt on completion of computation

For details, see [ESP32-S3 Technical Reference Manual > Chapter AES Accelerator](#).

---

**Subtitle: 4.1.4.3 RSA Accelerator**

The RSA Accelerator provides hardware support for high precision computation used in various RSA asymmetric cipher algorithms.

**Feature List**
- Large-number modular exponentiation with two optional acceleration options
- Large-number modular multiplication, up to 4096 bits
- Large-number multiplication, with operands up to 2048 bits
- Operands of different lengths
- Interrupt on completion of computation

For details, see [ESP32-S3 Technical Reference Manual > Chapter RSA Accelerator](#).

---

**Subtitle: 4.1.4.4 Secure Boot**

Secure Boot feature uses a hardware root of trust to ensure only signed firmware (with RSA-PSS signature) can be booted.

---

**Subtitle: 4.1.4.5 HMAC Accelerator**

The Hash-based Message Authentication Code (HMAC) module computes Message Authentication Codes (MACs) using Hash algorithm and keys as described in RFC 2104.

**Feature List**
- Standard HMAC-SHA-256 algorithm
- Hash result only accessible by configurable hardware peripheral (in downstream mode)
- Compatible to challenge-response authentication algorithm
- Generates required keys for the Digital Signature (DS) peripheral (in downstream mode)
- Re-enables soft-disabled JTAG (in downstream mode)

For details, see [ESP32-S3 Technical Reference Manual > Chapter HMAC Accelerator](#).

---

**Footer:**
Espressif Systems  
49  
[Submit Documentation Feedback](#)  
ESP32-S3 Series Datasheet v2.1