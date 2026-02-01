**Title: Functional Description**

---

### **4.1.3.11 Debug Assistant**

The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

#### Feature List

- Read/write monitoring: Monitors whether the CPU bus has read from or written to a specified address space. A detected read or write will trigger an interrupt.
  
- Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
  
- Program counter (PC) logging: Records PC value. The developer can get the last PC value at the most recent CPU reset.
  
- Bus access logging: Recorders the information about bus access. When the CPU or DMA writes a specified value, the Debug Assistant module will record the address and PC value of this write operation, and push the data to the SRAM.

For details, see [ESP32-C3 Technical Reference Manual > Chapter Debug Assistant (ASSIST_DEBUG)](#).

---

### **4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

#### 4.1.4.1 AES Accelerator

ESP32-C3 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-C3 has two working modes, which are Typical AES and DMA-AES.

#### Feature List

- **Typical AES working mode**
  - AES-128/AES-256 encryption and decryption
  
- **DMA-AES working mode**
  - AES-128/AES-256 encryption and decryption
  - Block cipher mode
    - ECB (Electronic Codebook)
    - CBC (Cipher Block Chaining)
    - OFB (Output Feedback)
    - CTR (Counter)
    - CFB8 (8-bit Cipher Feedback)

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C3 Series Datasheet v2.2

**Page Number: 42**