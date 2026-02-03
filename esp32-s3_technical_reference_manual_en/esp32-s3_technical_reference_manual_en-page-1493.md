**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header (with register address):**
Register 39.20. SENS_SAR_TOUCH_CONF_REG (0x005C)

**Table Description with Binary Representation of Register Bits:**

| Bit | Name                          |
|-----|-------------------------------|
| 31-28| SENS_TOUCH_APPROACH_PAD0      |
| 27-24| SENS_TOUCH_APPROACH_PAD1      |
| 23   | SENS_TOUCH_APPROACH_PAD2      |
| 22   | SENS_TOUCH_UNIT_END           |
| 21   | SENS_TOUCH_STATUS_CLR         |
| 20   | SENS TOUCH DATA SEL           |
| 19-18| SENS_TOUCHUnit End            |
| 17   | SENS_TOUCH_DENOISEEnd        |
| 16   | SENS_TOUCHUnit End            |
| 15   | SENS_TOUCHUnit End            |
| 14   | SENS TOUCHStatusCLR           |
| 0    | Reset                         |

**Description of Register Bits:**

- **SENS_TOUCH_OUTEN:** Enable touch controller output. (R/W)
- **SENS_TOUCH_STATUS_CLR:** Clear all touch active status. (WO)
- **SENS_TOUCH_DATA_SEL:** Select touch data mode. (R/W)

  - `0 and 1`: raw_data
  - `2`: benchmark
  - `3`: smooth data

- **SENS TOUCH DENOISE End:** Touch denoise done. (RO)

- **SENS_TOUCH_UNIT_END:** Indicate the completion of sampling. (RO)

- **SENS_TOUCH_APPROACH_PAD2, SENS_TOUCH_APPROACH_PAD1, SENS_TOUCH_APPROACH_PAD0:** Indicate which pin is selected as proximity pin 2., proximity pin 1., and proximity pin 0 respectively. (R/W)

**Section Header:**
Register 39.21. SENS_SAR_TOUCH_DENOISE_REG (0x0060)

**Table Description with Binary Representation of Register Bits for Denoise Data:**

| Bit | Name                          |
|-----|-------------------------------|
| 31   | reserved                      |
| 22-21| SENSTOUCH_DENOISE_DATA       |

**Description of Register Bits (for denoise data):**
- **SENS_TOUCH_DENOISE_DATA:** Denoise value measured from touch sensor O. (RO)

---

**Footer:**
Espressif Systems
Page number: 1493

Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)