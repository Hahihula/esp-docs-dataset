**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_OUT_W1TS_REG | GPIO 0-31 output register_W1TS | 0x3FF44008 | WO |
| GPIO_OUT_W1TC_REG | GPIO 0-31 output register_W1TC | 0x3FF4400C | WO |
| GPIO_OUT1_REG | GPIO 32-39 output register | 0x3FF44010 | R/W |
| GPIO_OUT1_WITS_REG | GPIO 32-39 output bit set register | 0x3FF44014 | WO |
| GPIO_OUT1_WTC_REG | GPIO 32-39 output bit clear register | 0x3FF44018 | WO |
| GPIO_ENABLE_REG | GPIO 0-31 output enable register | 0x3FF44020 | R/W |
| GPIO_ENABLE_WITS_REG | GPIO 0-31 output enable register_W1TS | 0x3FF44024 | WO |
| GPIO_ENABLE_WTC_REG | GPIO 0-31 output enable register_W1TC | 0x3FF44028 | WO |
| GPIO_ENABLE1_REG | GPIO 32-39 output enable register | 0x3FF4402C | R/W |
| GPIO_ENABLE1_WITS_REG | GPIO 32-39 output enable bit set register | 0x3FF44030 | WO |
| GPIO_ENABLE1_WTC_REG | GPIO 32-39 output enable bit clear register | 0x3FF44034 | WO |
| GPIO_STRAP_REG | Bootstrap pin value register | 0x3FF44038 | RO |
| GPIO_IN_REG | GPIO 0-31 input register | 0x3FF4403C | RO |
| GPIO_IN1_REG | GPIO 32-39 interrupt input register | 0x3FF44040 | R/W |
| GPIO_STATUS_REG | GPIO 0-31 interrupt status register | 0x3FF44044 | WO |
| GPIO_STATUS_WITS_REG | GPIO 0-31 interrupt status register_W1TS | 0x3FF44048 | RO |
| GPIO_STATUS_WTC_REG | GPIO 0-31 interrupt status register_W1TC | 0x3FF4404C | WO |
| GPIO_STATUS1_REG | GPIO 32-39 interrupt status register1 | 0x3FF44050 | R/W |
| GPIO_STATUS1_WITS_REG | GPIO 32-39 interrupt status bit set register | 0x3FF44054 | WO |
| GPIO_STATUS1_WTC_REG | GPIO 32-39 interrupt status bit clear register | 0x3FF44058 | R/W |
| GPIO_ACPU_INT_REG | GPIO 0-31 APP_CPU interrupt status | 0x3FF44060 | RO |
| GPIO_ACPU_NMI_INT_REG | GPIO 0-31 APP_CPU non-maskable interrupt status | 0x3FF44064 | R/W |
| GPIO_PCPU_INT_REG | GPIO 0-31 PRO_CPU interrupt status | 0x3FF44068 | RO |
| GPIO_PCPU_NMI_INT_REG | GPIO 0-31 PRO_CPU non-maskable interrupt status | 0x3FF4406C | R/W |
| GPIO_ACPU_INT1_REG | GPIO 32-39 APP_CPU interrupt status | 0x3FF44074 | RO |
| GPIO_ACPU_NMI_INT1_REG | GPIO 32-39 APP_CPU non-maskable interrupt status | 0x3FF44078 | R/W |
| GPIO_PCPU_INT1_REG | GPIO 32-39 PRO_CPU interrupt status | 0x3FF4407C | RO |
| GPIO_PCPU_NMI_INT1_REG | GPIO 32-39 PRO_CPU non-maskable interrupt status | 0x3FF44080 | R/W |
| GPIO_PINO_REG | Configuration for GPIO pin 0 | 0x3FF44088 | RO |
| GPIO_PIN1_REG | Configuration for GPIO pin 1 | 0x3FF4408C | W/R |
| GPIO_PIN2_REG | Configuration for GPIO pin 2 | 0x3FF44090 | R/W |
| ... | ... | ... | ... |
| GPIO_PIN38_REG | Configuration for GPIO pin 38 | 0x3FF44120 | W/R |
| GPIO_PIN39_REG | Configuration for GPIO pin 39 | 0x3FF44124 | R/W |
| GPIO_FUNC0_IN_SEL_CFG_REG | Peripheral function 0 input selection register | 0x3FF44130 | RO |
| GPIO_FUNC1_IN_SEL_CFG_REG | Peripheral function 1 input selection register | 0x3FF44134 | W/R |
| ... | ... | ... | ... |
| GPIO_FUNC254_IN_SEL_CFG_REG | Peripheral function 254 input selection register | 0x3FF44528 | R/W |
| GPIO_FUNC255_IN_SEL_CFG_REG | Peripheral function 255 input selection register | 0x3FF4452C | W/R |

---

*Espressif Systems*

*Page: 135*

*Document Version: ESP32 TRM (Version 5.6)*

*Submit Documentation Feedback*