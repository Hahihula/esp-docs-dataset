**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Body Text:**
corresponding summary bit is also cleared. When both summary bits are cleared, the interrupt signal connected to CPU is de-asserted (stops signalling).

Interrupts are not queued up, and if a new interrupt-event occurs before the driver has responded to it, no additional interrupts are generated. For example, the SDHOST_IDSTS_RI indicates that one or more data were transferred to the Host buffer.

An interrupt is generated only once for concurrent events. The driver must scan the **SDHOST_IDSTS_REG** register for the interrupt cause.

**Footer:**
Espressif Systems
1281 ESP32-S3 TRM (Version 1.7)

**Link Texts:**
GoBack, Submit Documentation Feedback