**Title: Functional Description**

---

### **4.1.4.4 RSA Accelerator**

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly improving their run time and reducing their software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly. The RSA accelerator also supports operands of different lengths, which provides more flexibility during the computation.

**Feature List**
- large-number modular exponentiation with two optional acceleration options
- large-number modular multiplication, up to 3072 bits
- large-number multiplication, with operands up to 1536 bits
- operands of different lengths
- interrupt on completion of computation

For details, see the [ESP32-C5 Technical Reference Manual > Chapter RSA Accelerator](#).

---

### **4.1.4.5 SHA Accelerator**

ESP32-C5 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared to SHA algorithms implemented solely in software. The SHA accelerator integrated in ESP32-C5 has two working modes, which are typical SHA and DMA-SHA.

**Feature List**
- the following hash algorithms introduced in [FIPS PUB 180-4](#)
  - SHA-1
  - SHA-224
  - SHA-256
  - SHA-384
  - SHA-512/224
  - SHA-512/256
  - SHA-512/t

**two working modes**
- typical SHA
- DMA-SHA

- interleaved function in typical SHA working mode
- interrupt function in DMA-SHA working mode

For more details, see the [ESP32-C5 Technical Reference Manual > Chapter SHA Accelerator (SHA)](#).

---

Espressif Systems  
46  
[Submit Documentation Feedback](#)  
[ESP32-C5 Series Datasheet v1.0](#)