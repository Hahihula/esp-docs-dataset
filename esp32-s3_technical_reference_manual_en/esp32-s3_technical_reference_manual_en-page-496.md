**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Table of Analog Functions for GPIO Pins**

| RTC GPIO Num | GPIO Num | Pin Name    | Analog Function |
|--------------|----------|-------------|-----------------|
|              |          |             |                 |
| 6            | 6        | GPIO6       | TOUCH6          | ADC1_CH5         |
| 7            | 7        | GPIO7       | TOUCH7          | ADC1_CH6         |
| 8            | 8        | GPIO8       | TOUCH8          | ADC1_CH7         |
| 9            | 9        | GPIO9       | TOUCH9          | ADC1_CH8         |
| 10           | 10       | GPIO10      | TOUCH10         | ADC1_CH9         |
| 11           | 11       | GPIO11      | TOUCH11         | ADC2_CH0         |
| 12           | 12       | GPIO12      | TOUCH12         | ADC2_CH1         |
| 13           | 13       | GPIO13      | TOUCH13         | ADC2_CH2         |
| 14           | 14       | GPIO14      | TOUCH14         | ADC2_CH3         |
| 15           | 15       | XTAL_32K_P  | XTAL_32K_P      | ADC2_CH4         |
| 16           | 16       | XTAL_32K_N  | XTAL_32K_N      | ADC2_CH5         |
| 17           | 17       | GPIO17      | -               | ADC2_CH6         |
| 18           | 18       | GPIO18      | -               | ADC2_CH7         |
| 19           | 19       | GPIO19      | USB_D-         | ADC2_CH8         |
| 20           | 20       | GPIO20      | USB_D+         | ADC2_CH9         |
| 21           | 21       | GPIO21      | -               | -               |

**Section Title:**
6.14 Register Summary

**Subsection Title and Description:**

**6.14.1 GPIO Matrix Register Summary**

The addresses in this section are relative to the GPIO base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                   | Description                                                                                     | Address       | Access |
|------------------------|--------------------------------------------------------------------------------------------------|---------------|--------|
| GPIO Configuration Registers |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |Arduino IDE |
| GPIO_BT_SELECT_REG    | GPIO bit select register                                                                        | 0x0000        | R/W    |
| GPIO_OUT_REG          | GPIOO ~ 31 output register                                                                       | 0x0004        | R/W    |
| GPIO_OUT_WITS_REG     | GPIOO ~ 31 output bit set register                                                                | 0x0008        | WO     |
| GPIO_OUT_WITC_REG     | GPIOO ~ 31 output bit clear register                                                              | 0x000c        | WO     |
| GPIO_OUTReg           | GPIO32 ~ 48 output register                                                                       | 0x0010        | R/W    |
| GPIO_OUT1_WITS_REG    | GPIO32 ~ 48 output bit set register                                                              | 0x0014        | WO     |
| GPIO_OUT1_WITC_REG    | GPIO32 ~ 48 output bit clear register                                                             | 0x0018        | WO     |
| GPIO_SDIO_SELECT_REG  | GPIO SDIO selection register                                                                      | 0x001c        | R/W    |
| GPIO_ENABLEReg        | GPIOO ~ 31 output enable register                                                                  | 0x0020        | R/W    |
| GPIO_ENABLE_WITSReg   | GPIOO ~ 31 output enable bit set register                                                          | 0x0024        | WO     |
| GPIO_ENABLE_WITCReg   | GPIOO ~ 31 output enable bit clear register                                                        | 0x0028        | WO     |
| GPIO ENABLE1Reg       | GPIO32 ~ 48 output enable register                                                                  | 0x002c        | R/W    |
| GPIO_ENABLE1_WITSReg  | GPIO32 ~ 48 output enable bit set register                                                          | 0x0030        | WO     |
| GPIO ENABLE1_WITCReg  | GPIO32 ~ 48 output enable bit clear register                                                        | 0x0034        | WO     |
| GPIO_STRAP_REG        | Strapping pin value register                                                                      | 0x0038        | RO     |

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback