**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Titles and Content:**

---

### **27.12 Interrupt**

Interrupts can be generated as a result of various events. The IDINTEN register contains all the bits that might cause an interrupt. The IDINTEN register contains an enable bit for each of the events that can cause an interrupt.

There are two groups of summary interrupts, "Normal" ones (bit8 NIS) and "Abnormal" ones (bit9 AIS), as outlined in the IDSTS register. Interrupts are cleared by writing 1 to the position of the corresponding bit. When all the enabled interrupts within a group are cleared, the corresponding summary bit is also cleared. When both summary bits are cleared, the interrupt signal dmac_intr_o is de-asserted (stops signalling).

Interrupts are not queued up, and if a new interrupt-event occurs before the driver has responded to it, no additional interrupts are generated. For example, the Receive Interrupt IDSTS[I] indicates that one or more data were transferred to the Host buffer.

An interrupt is generated only once for concurrent events. The driver must scan the IDSTS register for the interrupt cause.

---

### **27.13 Register Summary**

The addresses in this section are relative to the SD/MMC base address provided in Table 3.3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| CTRL_REG | Control register | 0x0000 | R/W |
| CLKDIV_REG | Clock divider configuration register | 0x0008 | R/W |
| CLKSRC_REG | Clock source selection register | 0x000C | R/W |
| CLKENA_REG | Clock enable register | 0x0010 | R/W |
| TMOUT_REG | Data and response timeout configuration register | 0x0014 | R/W |
| CTYPE_REG | Card bus width configuration register | 0x0018 | R/W |
| BLKSIZ_REG | Card data block size configuration register | 0x001C | R/W |
| BYTCNT_REG | Data transfer length configuration register | 0x0020 | R/W |
| INTMASK_REG | SDIO interrupt mask register | 0x0024 | R/W |
| CMDARG_REG | Command argument data register | 0x0028 | R/W |
| CMD_REG | Command and boot configuration register | 0x002C | R/W |
| RESPO_REG | Response data register | 0x0030 | RO |
| RESP1_REG | Long response data register | 0x0034 | RO |
| RESP2_REG | Long response data register | 0x0038 | RO |
| RESP3_REG | Long response data register | 0x003C | RO |
| MINTSTS_REG | Masked interrupt status register | 0x0040 | RO |
| RINTSTS_REG | Raw interrupt status register | 0x0044 | R/W |
| STATUS_REG | SD/MMC status register | 0x0048 | RO |
| FIFOth_REG | FIFO configuration register | 0x004C | R/W |
| CDetect_REG | Card detect register | 0x0050 | RO |
| WRTPRT_REG | Card write protection (WP) status register | 0x0054 | RO |

---

**Footer:**
Espressif Systems
609 ESP32 TRM (Version 5.6)
Submit Documentation Feedback