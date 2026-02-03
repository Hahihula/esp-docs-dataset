**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.50. RTC_GPIO_IN_REG (0x0024)

| Field | Description |
| --- | --- |
| RTC_GPIO_IN_NEXT | GPIO0 ~ 21 input value. Bit10 corresponds to GPIO0, bit11 corresponds to GPIO1, etc. Each bit represents a pin input value, 1 for high level, and 0 for low level. (RO) |

---

### Register 6.51. RTC_GPIO_PINn (n: 0-21) (0x0028+0x4*n)

| Field | Description |
| --- | --- |
| RTC_GPIO_PINn_WAKEUP_ENABLE | GPIO wake-up enable. This will only wake up the chip from Light-sleep. (R/W) |

---

### Pin driver selection

| Field | Description |
| --- | --- |
| RTC_GPIO_PINn_PAD_DRIVER | 0: normal output; 1: open drain. (R/W) |

### GPIO interrupt type selection

| Field | Description |
| --- | --- |
| RTC_GPIO_PINn_INT_TYPE | 0: GPIO interrupt disabled; 1: rising edge trigger; 2: falling edge trigger; 3: any edge trigger; 4: low level trigger; 5: high level trigger. (R/W) |

---

**Footer:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)

[Submit Documentation Feedback](#)