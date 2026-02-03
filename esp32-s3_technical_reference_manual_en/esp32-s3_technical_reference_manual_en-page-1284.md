**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Subtitle:**
34.13 Registers

**Body Text:**

The addresses in this section are relative to SD/MMC Host Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Register Description:**
Register 34.1, SDHOST_CTRL_REG (0x0000)

| Address | Bit Range | Name                          |
|---------|----------|-------------------------------|
| 31      | reserved | -                             |
| ...     | ...      | -                             |
| 25      | reserved | -                             |
| 24      | reserved | -                             |
| 23      | (reserved) | SDHOST_CEATA_DEVICE, INTERRUPT_STATUS |
|        |          | The power-on reset or any other reset to the CE-ATA device. After reset, the CE-ATA device's interrupt is usually disabled (nEN = 1). If the host enables the CE-ATA device’s interrupt, then software should set this bit.
| ...     | ...      | -                             |
| 0       | reserved | Reset                        |

**Description of Bits:**
- **SDHOST_CEATA_DEVICE, INTERRUPT_STATUS:** Software should appropriately write to this bit after the power-on reset or any other reset to the CE-ATA device. After reset, the CE-ATA device’s interrupt is usually disabled (nEN = 1). If the host enables the CE-ATA device's interrupt, then software should set this bit.

**SDHOST_SEND_AUTO_STOP_CCSD:**
HOST_SEND_CCSD bits together; SDHOST_SEND_AUTO_STOP_CCSD should not be set independently of send_ccsd. When set, SD/MMC automatically sends an internally-generated STOP command (CMD12) to the CE-ATA device. After sending this internally-generated STOP command, the Auto Command Done (ACD) bit in SDHOST_RINTSTS_REG is set and an interrupt is generated for the host; if ACD interrupt not masked.

**SDHOST_SEND_CCSD:**
When set, SD/MMC sends CCSD to CE-ATA device. Software sets this bit only if current command expecting CCS that is RW_BLK). If interrupts are enabled for the CE-ATA device once pattern sent to the device software automatically clears the SDHOST_SEND_CCSD bit and also sets Command Done (CD) in the SDHOST_RINTSTS_REG register, generates an interrupt host case. The Command Done interrupt not masked.

**Note:**
Once set it takes two card clock cycles drive CCSD on CMD line due this within boundary conditions CSD may be sent to CE-ATA device even if has signalled CCS (R/W)

**Continuation Note:** Continued on the next page...

**Footer Information:**
Espressif Systems
1284 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback