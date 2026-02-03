**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Section Header: Register 34.38. SDHOST_EMMC_DDR_REG (0x10C)**

- **Field Name and Description:**
  - `SDHOST_HS400_MODE_REG`
    - Set 1 to enable HS400 mode.
    - Access Type: Read/Write
    - Example Value in Hexadecimal Format:
      ```
      31 30       2   1     0
      0x00000000 0x00
      ```

- **Field Name and Description:**
  - `SDHOST_HALFSTARTBIT_REG`
    - Control for start bit detection mechanism duration of start bit.
    - Each bit refers to one slot. Set this bit to 1 for eMMC4.5 and above, set to 0 for SD applications.
    - For eMMC4.5, start bit can be:
      - `1'b0`: Full cycle
      - `1'b1`: less than one full cycle

---

**Section Header: Register 34.39. SDHOST_ENSHIFT_REG (0x110)**

- **Field Name and Description:**
  - `DHOST_ENABLE_SHIFT_REG`
    - Control for the amount of phase shift provided on the default enables in the design.
    - Two bits assigned for each card:
      - Access Type: Read/Write
      - Example Value in Hexadecimal Format (with reserved fields):
        ```
        31       4   3     0
        0x00000000 0x00
        ```

- **Field Description for bits within `DHOST_ENABLE_SHIFT_REG`:**
  - `2'b00`: Default phase shift.
  - `2'b01`: Enables shifted to next immediate positive edge.
  - `2'b10`: Enables shifted to next immediate negative edge.
  - `2'b11`: Reserved.

---

**Section Header: Register 34.40. SDHOST_BUFFIFO_REG (0x200)**

- **Field Name and Description:**
  - `SDHOST_BUFFIFO_REG`
    - CPU write and read transmit data by FIFO.
    - This register points to the current Data FIFO:
      - Access Type: Read Only
      - Example Value in Hexadecimal Format with reserved fields (not provided)

---

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Page Number and Submission Link: "Submit Documentation Feedback" at the bottom of each page

--- 

Note:
- The hexadecimal format values are shown with reserved fields indicated by `0x00` or similar.
- The diagrammatic representation is not provided, so only textual descriptions have been included as per instructions.