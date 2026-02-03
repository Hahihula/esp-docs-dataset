**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Back to Top Button:**
GoBack

**Register Information Section Header:**
Register 34.11. SDHOST_CMD_REG (0x002C)

**Bitfield Diagram Description with Labels and Values for Each Bit:**
- The diagram shows a bitfield layout of the register, labeled from top to bottom as follows:
  - 31
  - 30
  - 29
  - ...
  - 5
  - 4
  - 3
  - 2
  - 1
  - 0

**Bitfield Labels and Values:**
- SDHOST_START_CMD (reserved)
- SDHOST_USE_HOLE (reserved)
- SDHOST_CCSEXPECTED (reserved)
- SDHOST CARD_NUMBER (reserved)
- SDHOST START_AUTO_MODE (reserved)
- SDHOST SEND_ABORT_DATA_WRITE_EXPECTED
- SDHOST WAIT_FOR_DATA_CHECK_RESPONSE_LENGTH
- SDHOST TRANSFER_DATA
- SDHOST RESPONSE EXPECT
- SDHOST_CMD_INDEX

**Bitfield Values:**
- 0x00 Reset value is shown at the end of each bit.

**Section Title and Description with Subsections (SDHOST_START_CMD):**
- **Title:** SDHOST_START_CMD Start command. Once command is served by the CIU, this bit is automatically cleared.
- When this bit is set, host should not attempt to write to any command registers. If a write is attempted, hardware lock error is set in raw interrupt register.

**Subsection (SDHOST_USE_HOLE):**
- **Title:** SDHOST_USE_HOLE Use Hold Register. Read/Write
  - O: CMD and DATA sent to card bypassing HOLD Register;
  - 1: CMD and DATA sent to card through the HOLD Register

**Subsection (SDHOST_CCSEXPECTED):**
- **Title:** SDHOST_CCSEXPECTED
  - O: Interrupts are not enabled in CE-ATA device (nIEN = 1 in ATA control register), or command does not expect CCS from device;
  - 1: Interrupts are enabled in CE-ATA device (nIEN = 0), and RW_BLK command expects command completion signal from CE-ATA device.
  - If the command expects Command Completion Signal (CCS) from the CE-ATA device, software should set this control bit. SD/MMC sets Data Transfer Over (DTO) bit in RINTSTS register and generates interrupt to host if Data Transfer Over interrupt is not masked.

**Subsection (SDHOST_READ_CEATA DEVICE):**
- **Title:** Read access flag.
  - O: Host is not performing read access (RW_REG or RW_BLK) towards CE-ATA device;
  - 1: Host is performing read access (RW_REG or RW_BLK) towards CE-ATA device.

**Additional Information about the Register Bit:**
- Software should set this bit to indicate that CE-ATA device is being accessed for read transfer.
- This bit is used to disable read data timeout indication while performing CE-ATA read transfers. Maximum value of I/O transmission delay can be no less than 10 seconds.

**Note on Data Timing:**
SD/MMC should not indicate read data timeout while waiting for data from CE-ATA device

**Footer Information with Navigation Link and Document Version:**
Continued on the next page...

Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)