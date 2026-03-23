

```markdown
| GPIO Num | Pin Name | Analog Function 0 | Analog Function 1 |
|----------|----------|-------------------|-------------------|
| 3        | GPIO3    | -                 | ADC1_CH3          |
| 4        | MTMS     | -                 | ADC1_CH4          |

## 5.14 Register Summary

### 5.14.1 GPIO Matrix Register Summary

The addresses in this section are relative to the GPIO base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers**<br><br>GPIO_BT_SELECT_REG | GPIO bit select register | 0x0000 | R/W |
| GPIO_OUT_REG | GPIO output register | 0x0004 | R/W/SS |
| GPIO_OUT_W1TS_REG | GPIO output set register | 0x0008 | WT |
| GPIO_OUT_W1TC_REG | GPIO output clear register | 0x000C | WT |
| GPIO_ENABLE_REG | GPIO output enable register | 0x0020 | R/W/SS |
| GPIO_ENABLE_W1TS_REG | GPIO output enable set register | 0x0024 | WT |
| GPIO_ENABLE_W1TC_REG | GPIO output enable clear register | 0x0028 | WT |
| GPIO_STRAP_REG | pin strapping register | 0x0038 | RO |
| GPIO_IN_REG | GPIO input register | 0x003C | RO |
| GPIO_STATUS_REG | GPIO interrupt status register | 0x0044 | R/W/SS |
| GPIO_STATUS_W1TS_REG | GPIO interrupt status set register | 0x0048 | WT |
| GPIO_STATUS_W1TC_REG | GPIO interrupt status clear register | 0x004C | WT |
| GPIO_PCPU_INT_REG | GPIO PRO_CPU interrupt status register | 0x005C | RO |
| GPIO_STATUS_NEXT_REG | GPIO interrupt source register | 0x014C | RO |
| **Pin Configuration Registers**<br><br>GPIO_PINO_REG | GPIO pin0 configuration register | 0x0074 | R/W |
| GPIO_PIN1_REG | GPIO pin1 configuration register | 0x0078 | R/W |
| GPIO_PIN2_REG | GPIO pin2 configuration register | 0x007C | R/W |
| GPIO_PIN3_REG | GPIO pin3 configuration register | 0x0080 | R/W |
| GPIO_PIN4_REG | GPIO pin4 configuration register | 0x0084 | R/W |
| GPIO_PIN5_REG | GPIO pin5 configuration register | 0x0088 | R/W |
| GPIO_PIN6_REG | GPIO pin6 configuration register | 0x008C | R/W |
| GPIO_PIN7_REG | GPIO pin7 configuration register | 0x0090 | R/W |
| GPIO_PIN8_REG | GPIO pin8 configuration register | 0x0094 | R/W |
| GPIO_PIN9_REG | GPIO pin9 configuration register | 0x0098 | R/W |
| GPIO_PIN10_REG | GPIO pin10 configuration register | 0x009C | R/W |
| GPIO_PIN11_REG | GPIO pin11 configuration register | 0x00A0 | R/W |
| GPIO_PIN12_REG | GPIO pin12 configuration register | 0x00A4 | R/W |
| GPIO_PIN13_REG | GPIO pin13 configuration register | 0x00A8 | R/W |
| GPIO_PIN14_REG | GPIO pin14 configuration register | 0x00AC | R/W |
```