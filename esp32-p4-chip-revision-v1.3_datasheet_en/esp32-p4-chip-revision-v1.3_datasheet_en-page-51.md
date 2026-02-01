**Title: Functional Description**

---

### **4.1.4.15 Brown-out Detector**

With the Brown-out detector, ESP32-P4 monitors the voltage levels of pins VDD_ANA and VDD_BAT. If the voltage on these pins drops below the predefined threshold (defaulting to 2.7V), the detector triggers signals to shut down certain power-consuming blocks (e.g., flash), ensuring that the digital module has sufficient time to save and transfer important data.

**Feature List**
- Monitors the voltage level of pins VDD_ANA and VDD_BAT
- Two configurable monitoring modes
  - Mode 0: The brown-out detector triggers interrupts when the brown-out counter reaches the predefined threshold and selects the reset mode according to the configuration.
  - Mode 1: The brown-out detector triggers a system reset when the voltage falls below the threshold.

**Additional Features**
- Configurable voltage-monitoring thresholds
- Noise tolerance

---

### **4.1.5 Cryptography/Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

#### 4.1.5.1 AES Accelerator (AES)

ESP32-P4 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-P4 has two working modes, which are Typical AES and DMA-AES.

**Feature List**
- **Typical AES working mode:**
  - AES-128/AES-256 encryption and decryption
- **DMA-AES working mode:**
  - AES-128/AES-256 encryption and decryption

**Block cipher modes include:**
- ECB (Electronic Codebook)
- CBC (Cipher Block Chaining)
- OFB (Output Feedback)
- CTR (Counter)
- CFB8 (8-bit Cipher Feedback)
- CFB128 (128-bit Cipher Feedback)

---

Espressif Systems  
ESP32-P4 Series Datasheet v0.6

[Submit Documentation Feedback](#)