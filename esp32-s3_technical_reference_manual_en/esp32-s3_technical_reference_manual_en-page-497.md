**Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_IN_REG | GPIO0 ~ 31 input register | 0x003C | RO |
| GPIO_IN1_REG | GPIO32 ~ 48 input register | 0x0040 | RO |
| GPIO_PINO_REG | Configuration for GPIO pin 0 | 0x0074 | R/W |
| GPIO_PIN1_REG | Configuration for GPIO pin 1 | 0x0078 | R/W |
| GPIO_PIN2_REG | Configuration for GPIO pin 2 | 0x007C | R/W |
| ... | ... | ... | ... |
| GPIO_PIN46_REG | Configuration for GPIO pin 46 | 0x012C | R/W |
| GPIO_PIN47_REG | Configuration for GPIO pin 47 | 0x0130 | R/W |
| GPIO_PIN48_REG | Configuration for GPIO pin 48 | 0x0134 | R/W |
| GPIOFUNCO_IN_SEL_CFG_REG | Peripheral function 0 input selection register | 0x0154 | R/W |
| GPIOFUNC1_IN_SEL_CFG_REG | Peripheral function 1 input selection register | 0x0158 | R/W |
| GPIOFUNC2_IN_SEL_CFG_REG | Peripheral function 2 input selection register | 0x015C | R/W |
| ... | ... | ... | ... |
| GPIO_FUNC253_IN_SEL_CFG_REG | Peripheral function 253 input selection register | 0x0548 | R/W |
| GPIO_FUNC254_IN_SEL_CFG_REG | Peripheral function 254 input selection register | 0x054C | R/W |
| GPIO_FUNC255_IN_SEL_CFG_REG | Peripheral function 255 input selection register | 0x0550 | R/W |
| GPIO FUNC0_OUT_SEL_CFG_REG | Peripheral output selection for GPIO0 | 0x0554 | R/W |
| GPIOFUNC1_OUT_SEL_CFG_REG | Peripheral output selection for GPIO1 | 0x0558 | R/W |
| GPIOFUNC2_OUT_SEL_CFG_REG | Peripheral output selection for GPIO2 | 0x055C | R/W |
| ... | ... | ... | ... |
| GPIO_FUNC47_OUT_SEL_CFG_REG | Peripheral output selection for GPIO47 | 0x0610 | R/W |
| GPIOFUNC48_OUT_SEL_CFG_REG | Peripheral output selection for GPIO48 | 0x0614 | R/W |
| GPIO_CLOCK_GATE_REG | GPIO clock gating register | 0x062C | R/W |

**Interrupt Status Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_STATUS_REG | GPIO0 ~ 31 interrupt status register | 0x0044 | R/W |
| GPIOSTATUS1_REG | GPIO32 ~ 48 interrupt status register | 0x0050 | R/W |
| GPIO_CPU_INT_REG | GPIO0 ~ 31 CPU interrupt status register | 0x005C | RO |
| GPIO_CPU_NMI_INT_REG | GPIO0 ~ 31 CPU non-maskable interrupt status register | 0x0060 | RO |
| GPIO_CPU_INT1_REG | GPIO32 ~ 48 CPU interrupt status register | 0x0068 | RO |
| GPIO_CPU_NMI_INT1_REG | GPIO32 ~ 48 CPU non-maskable interrupt status register | 0x006C | R/W |

**Interrupt Configuration Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_STATUS_WITS_REG | GPIO0 ~ 31 interrupt status bit set register | 0x0048 | WO |
| GPIO_STATUS_WITC_REG | GPIO0 ~ 31 interrupt status bit clear register | 0x004C | WO |
| GPIOSTATUS1_WITS_REG | GPIO32 ~ 48 interrupt status bit set register | 0x0054 | WO |
| GPIOSTATUS1_WITC_REG | GPIO32 ~ 48 interrupt status bit clear register | 0x0058 | WO |

**GPIO Interrupt Source Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_STATUS_NEXTReg | GPIO0 ~ 31 interrupt source register | 0x014C | RO |
| GPIO_STATUS_NEXTrg | GPIO32 ~ 48 interrupt source register | 0x0150 | R/W |

**Version Register**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_DATE_REG | Version control register | 0x06FC | R/W |

---

Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback