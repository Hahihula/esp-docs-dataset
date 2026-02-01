**Title: Functional Description**

---

### **4.2.1.1 USB OTG**

ESP32-S2 features a full-speed USB OTG interface which is compliant with the USB 2.0 specification (Note that it does not support the faster 480 Mbit/s high-speed transfer mode). It has the following features:

- software-configurable endpoint settings and suspend/resume
- support for dynamic FIFO sizing
- support for session request protocol (SRP) and host negotiation protocol (HNP)
- a full-speed USB PHY integrated in the chip

For more information, please refer to ESP32-S2 Technical Reference Manual > Chapter USB On-The-Go (USB).

---

**Subtitle: Pin Assignment**

For details, see Section 2.3.6 Peripheral Pin Assignment.

---

### **4.2.1.2 Two-wire Automotive Interface**

ESP32-S2 has a TWAI® controller with the following features:

- compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- standard frame format (11-bit ID) and extended frame format (29-bit ID)
- bit rates from 1 Kbit/s to 1 Mbit/s
- multiple modes of operation: Normal, Listen Only, and Self-Test
- 64-byte receive FIFO
- special transmissions: single-shot transmissions and self reception
- acceptance filter (single and dual filter modes)
- error detection and handling: error counters, configurable error interrupt threshold, error code capture, arbitration lost capture

For more information, please refer to ESP32-S2 Technical Reference Manual > Chapter Two-wire Automotive Interface (TWAI).

---

**Subtitle: Pin Assignment**

For details, see Section 2.3.6 Peripheral Pin Assignment.

---

### **4.2.2 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.

---

### **4.2.2.1 ADC**

ESP32-S2 integrates two 12-bit SAR ADCs and supports measurements on 20 channels (analog-enabled pins). The ULP-coprocessor in ESP32-S2 is also designed to measure voltage. The ULP can operate while the main

---

**Footer:**
Espressif Systems  
44  
Submit Documentation Feedback  
ESP32-S2 Series Datasheet v1.8