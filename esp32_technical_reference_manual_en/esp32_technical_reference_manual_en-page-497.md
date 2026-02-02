**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.8. DM MAIN_EN_REG (0x001C)

**Continuation Notice:**
Continued from the previous page...

**Body Text with List of Registers and Descriptions:**

- **DMAIN_FBEE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Fatal Bus Error Interrupt is enabled. When this bit is reset, the Fatal Bus Error Enable Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_ETIE:** When this bit is set with an Abnormal Interrupt Summary Enable (Bit[15]), the Early Transmit Interrupt is enabled. When this bit is reset, the Early Transmit Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_RWTE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Receive Watchdog Timeout Interrupt is enabled. When this bit is reset, the Receive Watchdog Timeout Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_RSE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Receive Stopped Interrupt is enabled. When this bit is reset, the Receive Stopped Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_RBUE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Receive Buffer Unavailable Interrupt is enabled. When this bit is reset, the Receive Buffer Unavailable Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_RIE:** When this bit is set with Normal Interrupt Summary Enable (Bit[16]), the Receive Interrupt is enabled. When this bit is reset, the Receive Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_UIE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Transmit Underflow Interrupt is enabled. When this bit is reset, the Underflow Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_OIE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Receive Overflow Interrupt is enabled. When this bit is reset, the Overflow Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_TJTE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Transmit Jabber Timeout Interrupt is enabled. When this bit is reset, the Transmit Jabber Timeout Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_TBUE:** When this bit is set with Normal Interrupt Summary Enable (Bit 16), the Transmit Buffer Unavailable Interrupt is enabled. When this bit is reset, the Transmit Buffer Unavailable Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_TSE:** When this bit is set with Abnormal Interrupt Summary Enable (Bit[15]), the Transmission Stopped Interrupt is enabled. When this bit is reset, the Transmission Stopped Interrupt is disabled.
  - Access Mode: Read/Write

- **DMAIN_TIE:** When this bit is set with Normal Interrupt Summary Enable (Bit[16]), the Transmit Interrupt is enabled. When this bit is reset, the Transmit Interrupt is disabled.
  - Access Mode: Read/Write

**Footer Information:**
Espressif Systems
Page Number: 497
Document Title: ESP32 TRM (Version 5.6)
Feedback Link Texts:
- Submit Documentation Feedback