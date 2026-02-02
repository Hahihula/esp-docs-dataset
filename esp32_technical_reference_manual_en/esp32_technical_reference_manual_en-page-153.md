**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.44. RTCIO_RTC_GPIO_IN_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31-14 | Reserved |

#### RTCIO_RTC_GPIO_IN_NEXT
- **Description:** GPIO0-17 input value.
- **Bit Details:**
  - Bit14 is GPIO[0],
  - Bit15 is GPIO[1],
  - etc. Each bit represents a pin input value, with:
    - `1` for high level,
    - `0` for low level.

---

### Register 6.45. RTCIO_RTC_GPIO_PINn (R: n-0; W: 0x28+4*n)

| Bit | Description |
|-----|-------------|
| 31-9 | Reserved |

#### RTCIO_RTC_GPIO_PINn_WAKEUP_ENABLE
- **Description:** GPIO wake-up enable.
- **Functionality:** This will only wake up the ESP32 from Light-sleep.

#### RTCIO_RTC_GPIO_PINn_WAKEUP_ENABLE
- **Description:** GPIO interrupt type selection (R/W).

| Value | Description |
|-------|-------------|
| 0     | GPIO interrupt disable; |
| 1     | rising edge trigger; |
| 2     | falling edge trigger; |
| 3     | any edge trigger; |
| 4     | low level trigger; |
| 5     | high level trigger. |

#### RTCIO_RTC_GPIO_PINn_PAD_DRIVER
- **Description:** Pin driver selection.
- **Values:**
  - `0`: normal output;
  - `1`: open drain.

---

**Footer Information:**

Espressif Systems  
Page Number: 153  
Document Version: ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)