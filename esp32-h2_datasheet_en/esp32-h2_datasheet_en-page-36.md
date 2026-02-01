**Title: Functional Description**

---

### Feature List

- **Supports two different elliptic curves (P-192 and P-256)**
- **11 working modes that support Base Point Verification, Base Point Multiplication, Jacobian Point Verification, Jacobian Point Multiplication, and mod operations**
- High anti-attack performance. Each point multiplication calculation of the ECC accelerator consumes:
  - *the same amount of time*
  - *the same amount of power*

For details, see [ESP32-H2 Technical Reference Manual > Chapter ECC Accelerator (ECC)](#).

---

### Subtitle: HMAC Accelerator

**4.1.4.3 HMAC Accelerator**

The HMAC Accelerator (HMAC) module is designed to compute Message Authentication Codes (MACs) using the SHA-256 Hash algorithm and keys as described in RFC 2104. It provides hardware support for HMAC computations, significantly reducing software complexity and improving performance.

#### Feature List

- Standard HMAC-SHA-256 algorithm
- Compatibility with challenge-response authentication algorithm
- Generates required keys for the Digital Signature Algorithm (DSA) peripheral in downstream mode
- Re-enables soft-disabled JTAG in downstream mode
- Hash result only accessible by configurable hardware peripheral (in downstream mode)

For details, see [ESP32-H2 Technical Reference Manual > Chapter HMAC Accelerator (HMAC)](#).

---

### Subtitle: RSA Accelerator

**4.1.4.4 RSA Accelerator**

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly improving their run time and reducing their software complexity.

Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly.

#### Feature List

- Large-number modular exponentiation with two optional acceleration options, operands width up to 3072 bits
- Large-number modular multiplication, operands width up to 3072 bits
- Large-number multiplication, operands width up to 1536 bits
- Operands of different widths
- Interrupt on completion of computation

For details, see [ESP32-H2 Technical Reference Manual > Chapter RSA Accelerator (RSA)](#).

---

**Footer:**
Espressif Systems  
Page number: **36**  
Document title: ESP32-H2 Series Datasheet v1.2  
Link to submit documentation feedback available at the bottom of each page.

(Note: The text marked with `#` is a placeholder for hyperlinks that are not displayed in this format.)