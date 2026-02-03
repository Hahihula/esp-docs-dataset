**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Navigation Link:**
GoBack

**Section Header:**
Register 34.33. SDHOST_IDSTS_REG (0x008C)

**Continuation Note:**
Continued from the previous page...

**Body Text with Definitions and Descriptions of Register Bits:**

- **SDHOST_IDSTS_CES**: Card Error Summary.
  - Indicates the status of the transaction to/from the card, also present in RINTSTS. 
  - Indicates the logical OR of the following bits:
    - EBE : End Bit Error;
    - RTO : Response Timeout/Boot Ack Timeout;
    - RCRC : Response CRC;
    - SBE : Start Bit Error;
    - DRTO : Data Read Timeout/BDS timeout;
    - DCRC : Data CRC for Receive;
    - RE : Response Error.
  - Writing 1 clears this bit. The abort condition of the IDMAC depends on the setting of this CES bit.

- **SDHOST_IDSTS_DU**: Descriptor Unavailable Interrupt.
  - This bit is set when the descriptor is unavailable due to OWNER bit = 0 (DESO[31] = 0).
  - Writing 1 clears this bit. 

- **SDHOST_IDSTS_FBE**: Fatal Bus Error Interrupt.
  - Indicates that a Bus Error occurred (IDSTS[12:10]).
  - When this bit is set, the DMA disables all its bus accesses.

- **SDHOST_IDSTS_RI**: Receive Interrupt.
  - Indicates the completion of data reception for a descriptor. 
  - Writing 1 clears this bit. 

- **SDHOST_IDSTS_TI**: Transmit Interrupt.
  - Indicates that data transmission is finished for a descriptor.
  - Writing 1 clears this bit.

**Footer:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback