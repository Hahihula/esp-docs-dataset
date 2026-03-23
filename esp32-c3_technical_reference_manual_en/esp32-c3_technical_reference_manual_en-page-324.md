

```markdown
| Peripherals                                 | Privileged Environment                  | Unprivileged Environment                 | Bit³   |
|---------------------------------------------|------------------------------------------|------------------------------------------|--------|
| GDMA                                        | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [7:6]  |
| eFuse Controller & PMU¹                     | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [15:14]|
| IO_MUX                                     | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [17:16]|
| GPIO                                       | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [7:6]  |
| Interrupt Matrix                            | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [21:20]|
| System Timer                               | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [31:30]|
| Timer Group 0                              | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [27:26]|
| Timer Group 1                              | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [29:28]|
| System Registers                           | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [17:16]|
| PMS Registers                              | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [19:18]|
| Debug Assist                               | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [27:26]|
| Accelerators²                              | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [5:4]  |
| Cache & XTS_AES¹                           | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [25:25]|
| UART 0                                     | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [1:0]  |
| UART 1                                     | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [31:30]|
| SPI 0                                      | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [5:4]  |
| SPI 1                                      | **_PMS_CONSTRAN_1_REG**                 | **_PMS_CONSTRAN_5_REG**                 | [3:2]  |
| SPI 2                                      | **_PMS_CONSTRAN_3_REG**                 | **_PMS_CONSTRAN_7_REG**                 | [1:0]  |
| I2C 0                                      | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [5:4]  |
| I2S                                        | **_PMS_CONSTRAN_3_REG**                 | **_PMS_CONSTRAN_7_REG**                 | [15:14]|
| USB OTG Core                               | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [15:14]|
| Two-wire Automotive Interface              | **_PMS_CONSTRAN_3_REG**                 | **_PMS_CONSTRAN_7_REG**                 | [11:10]|
| UHCI 0                                     | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [7:6]  |
| LED PWM Controller                         | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [17:16]|
| Remote Control Peripheral                  | **_PMS_CONSTRAN_2_REG**                 | **_PMS_CONSTRAN_6_REG**                 | [11:10]|
| APB Controller                             | **_PMS_CONSTRAN_3_REG**                 | **_PMS_CONSTRAN_7_REG**                 | [5:4]  |
| ADC Controller                             | **_PMS_CONSTRAN_4_REG**                 | **_PMS_CONSTRAN_8_REG**                 | [9:8]  |

---

¹ : This is shared by more than one peripherals.
² : Accelerators: AES, SHA, RSA, Digital Signatures, HMAC
³ : Access: R/W
⁴ : ** in the table replaces PMS_CORE_O_PIF.

## 14.5.2 Split Peripheral Regions into Split Regions

On top of what described in the previous section, user can select one of ESP32-C3’s peripheral region to split them into 7 regions (from Peri Region0 ~ Peri Region7) for more flexible permission control.

For example, the registers for ESP32-C3’s GDMA controller are allocated as:

*   3 sets of registers for each of 3 RX channel
*   3 sets of registers for each of 3 TX channel
*   1 set of registers for configuration

Espressif Systems
```