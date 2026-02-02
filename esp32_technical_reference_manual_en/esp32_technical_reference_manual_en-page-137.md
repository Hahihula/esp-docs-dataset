Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

---

**Name:**  
IO_MUX_UOTXD_REG

**Description:**  
Configuration register for UOTXD

**Address:**  
0x3FF49088  

**Access:**  
R/W

---

**Name:**  
IO_MUX_GPIO23_REG

**Description:**  
Configuration register for GPIO23

**Address:**  
0x3FF4908C  

**Access:**  
R/W

---

Subtitle: 6.12.3 RTC IO MUX Register Summary

---

**Table Title:** Table 6.12-3. RTC IO MUX Register Summary

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO configuration / data registers | | | |
| RTCIO_RTC_GPIO_OUT_REG | RTC GPIO output register | 0x3FF48400 | R/W |
| RTCIO_RTC_GPIO_OUT_W1TS_REG | RTC GPIO output bit set register | 0x3FF48404 | WO |
| RTCIO_RTC_GPIO_OUT_W1TC_REG | RTC GPIO out bit clear register | 0x3FF48408 | WO |
| RTCIO_RTC_GPIO_ENABLE_REG | RTC GPIO output enable register | 0x3FF4840C | R/W |
| RTCIO_RTC_GPIO_ENABLE_W1TS_REG | RTC GPIO output enable bit set register | 0x3FF48410 | WO |
| RTCIO_RTC_GPIO_ENABLE_W1TC_REG | RTC GPIO output enable bit clear register | 0x3FF48414 | WO |
| RTCIO_RTC_GPIO_STATUS_REG | RTC GPIO interrupt status register | 0x3FF48418 | WO |
| RTCIO_RTC_GPIO_STATUS_W1TS_REG | RTC GPIO interrupt status bit set register | 0x3FF4841C | WO |
| RTCIO_RTC_GPIO_STATUS_W1TC_REG | RTC GPIO interrupt status bit clear register | 0x3FF48420 | WO |
| RTCIO_RTC_GPIO_IN_REG | RTC GPIO input register | 0x3FF48424 | RO |
| RTCIO_RTC_GPIO_PIN0_REG | RTC configuration for pin 0 | 0x3FF48428 | R/W |
| RTCIO_RTC_GPIO_PIN1_REG | RTC configuration for pin 1 | 0x3FF4842C | R/W |
| RTCIO_RTC_GPIO_PIN2_REG | RTC configuration for pin 2 | 0x3FF48430 | R/W |
| RTCIO_RTC_GPIO_PIN3_REG | RTC configuration for pin 3 | 0x3FF48434 | R/W |
| RTCIO_RTC_GPIO_PIN4_REG | RTC configuration for pin 4 | 0x3FF48438 | R/W |
| RTCIO_RTC_GPIO_PIN5_REG | RTC configuration for pin 5 | 0x3FF4843C | R/W |
| RTCIO_RTC_GPIO_PIN6_REG | RTC configuration for pin 6 | 0x3FF48440 | R/W |
| RTCIO_RTC_GPIO_PIN7_REG | RTC configuration for pin 7 | 0x3FF48444 | R/W |
| RTCIO_RTC_GPIO_PIN8_REG | RTC configuration for pin 8 | 0x3FF48448 | R/W |
| RTCIO_RTC_GPIO_PIN9_REG | RTC configuration for pin 9 | 0x3FF4844C | R/W |
| RTCIO_RTC_GPIO_PIN10_REG | RTC configuration for pin 10 | 0x3FF48450 | R/W |
| RTCIO_RTC_GPIO_PIN11_REG | RTC configuration for pin 11 | 0x3FF48454 | R/W |
| RTCIO_RTC_GPIO_PIN12_REG | RTC configuration for pin 12 | 0x3FF48458 | R/W |
| RTCIO_RTC_GPIO_PIN13_REG | RTC configuration for pin 13 | 0x3FF4845C | R/W |
| RTCIO_RTC_GPIO_PIN14_REG | RTC configuration for pin 14 | 0x3FF48460 | R/W |
| RTCIO_RTC_GPIO_PIN15_REG | RTC configuration for pin 15 | 0x3FF48464 | R/W |
| RTCIO_RTC_GPIO_PIN16_REG | RTC configuration for pin 16 | 0x3FF48468 | R/W |
| RTCIO_RTC_GPIO_PIN17_REG | RTC configuration for pin 17 | 0x3FF4846C | R/W |
| RTCIO_DIG_PAD_HOLD_REG | RTC GPIO hold register | 0x3FF48474 | R/W |

**GPIO RTC function configuration registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTCIO_SENSOR_PADS_REG | Sensor pins configuration register | 0x3FF4847C | R/W |
| RTCIO_ADC_PAD_REG | ADC configuration register | 0x3FF48480 | R/W |

---

Footer: Espressif Systems  
Page number and document version information:
ESP32 TRM (Version 5.6)  

Link text at the bottom right corner of each page for submitting feedback or going back to a previous section.

(Note: The content above is transcribed as it appears in the image, including any potential typographical errors.)