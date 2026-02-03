**Title:**
Chapter 22 Digital Signature (DS)

**Subtitle:**
22.6 Registers

**Body Text:**
The addresses in this section are relative to the Digital Signature base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection Title:**
Register 22.1. DS_IV_m_REG (m: 0-3) (0x0630+4*m)

**Table Description for Register 22.1:**
- **DS_IV_m_REG (m: 0-3):** Address range is from m to the last bit of address.
- **0x00000000:** Value at a specific memory location.

**Subsection Title:**
Register 22.2. DS_SET_START_REG (0x0E00)

**Table Description for Register 22.2:**
- **DS_SET_START:** A register with bits set to indicate the start of certain operations.
- **(reserved):** Bits are reserved and not used.

**Subsection Title:**
Register 22.3. DS_SET_ME_REG (0x0E04)

**Table Description for Register 22.3:**
- **DS_SET_ME:** A register with bits set to start the Digital Signature operation.
- **(reserved):** Bits are reserved and not used.

**Additional Information in Body Text:**
- "Write 1 to this register to activate the DS peripheral." (WO)
- "Write 1 to this register to start DS operation. (WO)"

**Footer:**
Espressif Systems
905 ESP32-S3 TRM (Version 1.7)

**Link:**
Submit Documentation Feedback