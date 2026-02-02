**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.6. DMASTATUS_REG (0x0014)

**Continuation Note:**
Continued from the previous page...

**Subsection Heading with Code Block and Description:**
NORM_INT_SUMM
- **Description:** Normal Interrupt Summary bit value is the logical OR of the following bits when the corresponding interrupt bits are enabled in Interrupt Enable Register:(R/SS/WC)
  - Bit[0]: Transmit Interrupt.
  - Bit[2]: Transmit Buffer Unavailable.
  - Bit[6]: Receive Interrupt.

**Subsection Heading with Code Block and Description:**
Bit[14]: Early Receive Interrupt. Only unmasked bits affect the Normal Interrupt Summary bit. This is a sticky bit and must be cleared (by writing 1 to this bit) each time a corresponding bit, which causes NIS to be set, is cleared.

**Subsection Heading with Code Block and Description:**
ABN_INT_SUMM
- **Description:** Abnormal Interrupt Summary bit value is the logical OR of the following when the corresponding interrupt bits are enabled in Interrupt Enable Registers: (R/SS/WC)
  - Bit[1]: Transmit Process Stopped.
  - Bit[3]: Transmit Jabber Timeout.
  - Bit[4]: Receive FIFO Overflow.
  - Bit[5]: Transmit Underflow.
  - Bit[7]: Receive Buffer Unavailable. Bit[8]: Receive Process Stopped.
  - Bit[9]: Receive Watchdog Timeout.
  - Bit[10]: Early Transmit Interrupt.

**Subsection Heading with Code Block and Description:**
Bit[13]: Fatal Bus Error. Only unmasked bits affect the Abnormal Interrupt Summary bit. This is a sticky bit and must be cleared (by writing 1 to this bit) each time a corresponding bit, which causes AIS to be set, is cleared.

**Subsection Heading with Code Block and Description:**
EARLY_RECV_INT
- **Description:** This bit indicates that the DMA filled the first data buffer of the packet. This bit is cleared when the software writes 1 to this bit or when Bit[6] (RI) of this register is set (whichever occurs earlier). (R/SS/WC)

**Subsection Heading with Code Block and Description:**
FATAL BUS ERR_INT
- **Description:** This bit indicates that a bus error occurred, as described in Bits [25:23]. When this bit is set, the corresponding DMA engine disables all of its bus accesses. (R/SS/WC)

**Subsection Heading with Code Block and Description:**
EARLYTrans_INT
- **Description:** This bit indicates that the frame to be transmitted is fully transferred to the MTL Transmit FIFO. (R/SS/WC)

**Subsection Heading with Code Block and Description:**
RECV_WDT_TO
- **Description:** When set, this bit indicates that the Receive Watchdog Timer expired while receiving the current frame and the current frame is truncated after the watchdog timeout. (R/SS/WC)

**Continuation Note at Bottom of Page:**
Continued on the next page...

**Footer Information:**
Espressif Systems
492 ESP32 TRM (Version 5.6)
Submit Documentation Feedback