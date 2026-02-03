**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Header:**
Register 34.30. SDHOST_BMOD_REG (0x0080)

**Hexadecimal Address Diagrams and Labels for Register 34.30, SDHOST_BMOD_REG:**

- The diagram shows the layout of register bits with labels such as "SDHOST_BMOD_PBL", "SDHOST_BMOD_FB", etc.

**Register Description - SDHOST_BMOD_REG (0x0080):**
- **Field Name:** SDHOST_BMOD_PBL
  - **Description:** Programmable Burst Length. These bits indicate the maximum number of beats to be performed in one IDMAC transaction.
  - **Explanation:** The IDMAC will always attempt to burst as specified by PBL each time it starts a burst transfer on the host bus.

**Values for SDHOST_BMOD_PBL:**
- Permissible values are listed (1, 4, 8, 16, 32, 64, 128 and 256).
- This value is described as being mirrored in MSIZE of FIFO register.
- To change this value, write the required value to FIFOH register.

**Field Name:** SDHOST_BMOD_PBL (continued)
- **Values:**
  - `000`: 1-byte transfer
  - `001`: 4-byte transfer
  - `010`: 8-byte transfer
  - `011`: 16-byte transfer

**Field Name:** SDHOST_BMOD_PBL (continued)
- **Values:**
  - `100`: 32-byte transfer
  - `101`: 64-byte transfer
  - `110`: 128-byte transfer
  - `111`: 256-byte transfer

**Field Name:** PBL (continued)
- **Description:**
  - "PBL is a read-only value and applicable only for data access, it does not apply to descriptor access."

**Field Name:** SDHOST_BMOD_DE
  - **Description:** IDMAC Enable. When set, the IDMAC is enabled.

**Field Name:** SDHOST_BMOD_FB
  - **Description:**
    - "Controls whether the AHB Master interface performs fixed burst transfers or not."
    - Set to use only SINGLE, INCR4, INCR8 or INCR16 during start of normal burst transfers.
    - When reset, uses SINGLE and INCR burst transfer operations.

**Field Name:** SDHOST_BMOD_SWR
  - **Description:**
    - "Software Reset. When set, the DMA Controller resets all its internal registers."
    - Automatically cleared after one clock cycle (R/W).

**Register Description for Register 34.31, SDHOST_PLDMND_REG (0x0080):**

- This register is described as having a role in "Roll Demand".
- If the OWNER bit of a descriptor isn't set, the FSM goes to Suspend state.
- The host needs to write any value into this register for IDMAC FSM to resume normal descriptor fetch operation.

**Field Name:** SDHOST_PLDMND_REG
  - **Description:**
    - "Roll Demand. If the OWNER bit of a descriptor is not set, the FSM goes to the Suspend state."
    - The host needs to write any value into this register for IDMAC FSM to resume normal descriptor fetch operation.
    - This field has read-only access (WO).

**Footer Information:**
- Page number 31
- Document version information at bottom right corner:
  - "ESP32-S3 TRM (Version 1.7)"
- Company name and document submission feedback link are also present.

This detailed description captures all the textual content from the image, including register descriptions with their respective fields' functionalities in a structured format as requested by your instructions.