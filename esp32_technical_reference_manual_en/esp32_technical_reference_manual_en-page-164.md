**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.56. RTCIO_XTL_EXT_CTR_REG (0x0CCO)

| Bit | Description |
|-----|-------------|
| 31-27 | Reserved |
| 26   | Reset |
| 0    | Reset |

**Description:**
RTCIO_XTL_EXT_CTR_SEL
Select the external crystal power down enable source to get into sleep mode. 
- `0`: select GPIO0;
- `1`: select GPIO2, etc.
The input value on this pin XOR RTC_CNTL_XTL_EXT_CTR_LV is the crystal power down enable signal.

**Access:** (R/W)

---

### Register 6.57. RTCIO_SAR_I2C_IO_REG (0x0CC4)

| Bit | Description |
|-----|-------------|
| 31-29 | Reserved |
| 28   | Reset |
| 0    | Reset |

**Description:**
RTCIO_SAR_I2C_SDA_SEL
Selects the other pin as the RTC I2C SDA signal.
- `0`: pin TOUCH_PAD[1];
- Default value is `0`. (R/W)

RTCIO_SAR_I2C_SCL_SEL
Selects the other pin as the RTC I2C SCL signal.
- `0`: pin TOUCH_PAD[0];
- Default value is `0`. (R/W)

---

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback