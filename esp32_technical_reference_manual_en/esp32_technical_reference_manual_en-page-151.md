**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.38. RTCIO_RTC_GPIO_ENABLE_REG (0x000C)

| Bit | Description |
|-----|-------------|
| 14-13 | Reserved |

RTCIO_RTC_GPIO_ENABLE REG  
[Binary representation of the register]  

**Description:**  
RTCIO_RTC_GPIO_ENABLE_REG GPIOO-17 output enable. Bit14 is GPIO[0], bit15 is GPIO[1], etc. This means this GPIO pin is output (R/W).

---

### Register 6.39. RTCIO_RTC_GPIO_ENABLE_W1TS_REG (0x0010)

| Bit | Description |
|-----|-------------|
| 14-13 | Reserved |

RTCIO_RTC_GPIO_ENABLE WITS  
[Binary representation of the register]  

**Description:**  
RTCIO_RTC_GPIO_ENABLE_WITS GPIOO-17 output enable set register. For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_ENABLE will be set (WO).

---

### Register 6.40. RTCIO_RTC_GPIO_ENABLE_W1TC_REG (0x0014)

| Bit | Description |
|-----|-------------|
| 14-13 | Reserved |

RTCIO_RTC_GPIO_ENABLE W1TC  
[Binary representation of the register]  

**Description:**  
RTCIO_RTC_GPIO_ENABLE_W1TC GPIOO-17 output enable clear register. For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_ENABLE will be cleared (WO).

---

*Footer:* Espressif Systems  
Submit Documentation Feedback ESP32 TRM (Version 5.6)