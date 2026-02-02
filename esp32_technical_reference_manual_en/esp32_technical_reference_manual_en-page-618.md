**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Section Header:**
Register 27.11. CMD_REG (0x002C)

**Continuation Note:**
Continued from the previous page ...

**Subsection - TRANSFER_MODE (R/W):**
- **Description:**
  O: Block data transfer command;
  1: Stream data transfer command. Don't care if no data expected.

**Subsection - READWRITE (R/W):**
- **Description:**
  O: Read from card;
  1: Write to card.
  Note: "Don’t care if no data is expected from card."

**Subsection - DATAEXPECTED (R/W):**
- **Description:**
  O: No data transfer expected.
  1: Data transfer expected.

**Subsection - CHECK_RESPONSE_CRC (R/W):**
- **Description:**
  O: Do not check;
  1: Check response CRC. Some of command responses do not return valid CRC bits. Software should disable CRC checks for those commands in order to disable CRC checking by controller.

**Subsection - RESPONSE_LENGTH (R/W):**
- **Description:**
  O: Short response expected from card;
  1: Long response expected from card.

**Subsection - RESPONSEEXPECT (R/W):**
- **Description:**
  O: No response expected from card;
  1: Response expected from card.

**Subsection - CMD_INDEX Command index. (R/W):**

---

**Section Header:**
Register 27.12. RESPO_REG (0x0030)

**Field Description for RESPO_REG Bit[31:0] of response. (RO):**
- **Reset Value:** Reset

**Field Description for RESP1_REG Bit[63:32] of long response. (RO):**
- **Reset Value:** Reset

---

**Footer Information:**
Espressif Systems
Page 618 ESP32 TRM (Version 5.6)
Submit Documentation Feedback