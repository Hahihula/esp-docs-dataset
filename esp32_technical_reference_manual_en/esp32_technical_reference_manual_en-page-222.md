**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Header:**
Register 9.39. RTC_CNTL_BROWN_OUT_REG (0x0D4)

**Table Description:**
- The table lists various registers related to brownout detection and their bit positions.
- Columns include register names, offset within the register, width in bits.

**Register Descriptions with Details:**

1. **RTC_CNTL_BROWN_OUT_DET**
   - **Description:** Brownout detect (RO)
   - **Access Type:** Read-only

2. **RTC_CNTL_BROWN_OUT_ENA**
   - **Description:** Enables brownout (R/W)

3. **RTC_CNTL_DBROWN_OUT_THRES**
   - **Description:** Brownout threshold.
     - When the supply voltage is approximately below this level, the brownout detector will reset the chip
     - Note that there may be some variation of brownout voltage levels between each ESP32 chip.

4. **RTC_CNTL_BROWN_OUT_FIRST_ENA**
   - **Description:** Enables brownout reset (R/W)

5. **RTC_CNTL_BROWN_OUT_FIRST_WAIT**
   - **Description:** Brownout reset wait cycles.
     - Access Type: Read/Write

6. **RTC_CNTL_BROWN_OUT_PD_RF_ENA**
   - **Description:** Enables power down RF when brownout happens.

7. **RTC_CNTL_BROWN_OUT_CLOSE_FLASH_ENA**
   - **Description:** Sends suspend command to flash when brownout happens (R/W)

**Footer:**
- Page number and document version information:
  - "222 ESP32 TRM (Version 5.6)"
- Company name at the bottom left corner.
- Link for submitting documentation feedback.

**Navigation Links:**
- GoBack button in blue text on top right side of page header, indicating a navigation option to go back from this section or document view.