**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Section Header: Register 27.27. BMOD_REG (0x0080)**

- **BMOD_PBL Programmable Burst Length**: These bits indicate the maximum number of beats to be performed in one IDMAC transaction. The IDMAC will always attempt to burst as specified in PBL each time it starts a burst transfer on the host bus. The permissible values are 1, 4, 8, 16, 32, 64, 128 and 256. This value is the mirror of MSIZE of FIFO register. In order to change this value, write the required value to FIFOth register.
  - **Value Encoding**:
    - `000`: 1-byte transfer
    - `001`: 4-byte transfer
    - `010`: 8-byte transfer
    - `011`: 16-byte transfer
    - `100`: 32-byte transfer
    - `101`: 64-byte transfer
    - `110`: 128-byte transfer
    - `111`: 256-byte transfer

- **BMOD_PBL is a read-only value and applicable only for data access, it does not apply to descriptor access. (R/W)**

- **BMOD_DE IDMAC Enable**: When set, the IDMAC is enabled.
  - `(R/W)`

- **BMOD_FB Fixed Burst**: Controls whether the AHB Master interface performs fixed burst transfers or not. When set, the AHB will use only SINGLE, INCR4, INCR8 or INCR16 during start of normal burst transfers. When reset, the AHB will use SINGLE and INCR burst transfer operations.
  - `(R/W)`

- **BMOD_SWR Software Reset**: When set, the DMA Controller resets all its internal registers. It is automatically cleared after one clock cycle.
  - `(R/W)`

**Section Header: Register 27.28. PLDMND_REG (0x0080)**

- **PLDMND_REG Poll Demand**: If the OWN bit of a descriptor is not set, the FSM goes to the Suspend state. The host needs to write any value into this register for the IDMAC FSM to resume normal descriptor fetch operation.
  - This is a write only register, PD bit is write-only.

**Section Header: Register 27.29. DBADDR_REG (0x0088)**

- **DBADDR_REG Start of Descriptor List**: Contains the base address of the First Descriptor. The LSB bits [1:0] are ignored and taken as all-zero by the IDMAC internally.
  - Hence these LSB bits may be treated as read-only.

**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

---

(Note: The text is transcribed from a technical document, so some parts are described in markdown format to represent the structure and content.)