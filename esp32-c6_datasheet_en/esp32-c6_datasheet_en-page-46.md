**Title: Functional Description**

---

### **4.1.3.12 Debug Assistant**

The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

#### Feature List

- Read/write monitoring: Monitor whether the HP CPU bus reads from or writes to a specified memory address space
- Stack pointer (SP) monitoring: Prevent stack overflow or erroneous push/pop operations violation will trigger an interrupt.
- Program counter (PC) logging: Record PC value. The developer can get the last PC value at the most recent HP CPU reset
- Bus access logging: Record information about bus access when the HP CPU, LP CPU, or DMA writes a specified value

For details, see [ESP32-C6 Technical Reference Manual](#) > Chapter Debug Assistant (ASSIST_DEBUG).

---

### **4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

#### 4.1.4.1 AES Accelerator

ESP32-C6 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-C6 has two working modes, which are Typical AES and DMA-AES.

##### Feature List

- **Typical AES working mode**
  - AES-128/AES-256 encryption and decryption
- **DMA-AES working mode**
  - AES-128/AES-256 encryption and decryption
- Block cipher mode
  * ECB (Electronic Codebook)
  * CBC (Cipher Block Chaining)
  * OFB (Output Feedback)
  * CTR (Counter)
  * CFB8 (8-bit Cipher Feedback)

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C6 Series Datasheet v1.4

--- 

**Page Number:** 46