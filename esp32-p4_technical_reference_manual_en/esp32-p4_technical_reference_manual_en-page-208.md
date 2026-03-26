

```markdown
## Register 3.4. mie (0x304)

| Bit | Field Name       | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)      |                                                                             |
| 30  | HP_IE            | Write 1 to enable HP interrupt. (R/W)                                      |
| 29  | LP_RTC_IE        | Write 1 to enable RTC interrupt. (R/W)                                     |
| 28  | LP_WDT_IE        | Write 1 to enable WDT interrupt. (R/W)                                     |
| 27  | LP_TIMER_IE      | Write 1 to enable LP Timer interrupt. (R/W)                                |
| 26  | LP_MB_IE         | Write 1 to enable Mailbox interrupt. (R/W)                                 |
| 25  | LP_PMU_IE        | Write 1 to enable PMU interrupt. (R/W)                                     |
| 24  | LP_ANAPERI_IE    | Write 1 to enable ANAPERI interrupt. (R/W)                                 |
| 23  | LP_SYSREG_IE     | Write 1 to enable SYSREG interrupt. (R/W)                                  |
| 22  | LP_EFUSE_IE      | Write 1 to enable LP eFuse interrupt. (R/W)                                |
| 21  | LP_TSENS_IE      | Write 1 to enable LP TSENS interrupt. (R/W)                                |
| 20  | LP_TOUCH_IE      | Write 1 to enable LP TOUCH interrupt. (R/W)                                |
| 19  | LP_ADC_IE        | Write 1 to enable LP ADC interrupt. (R/W)                                  |
| 18  | LP_GPIO_IE       | Write 1 to enable LP GPIO interrupt. (R/W)                                 |
| 17  | LP_I2C_IE        | Write 1 to enable I2C interrupt. (R/W)                                     |
| 16  | LP_SPI_IE        | Write 1 to enable LP SPI interrupt. (R/W)                                  |
| 15  | LP_UART_IE       | Write 1 to enable LP UART interrupt. (R/W)                                 |
| 14  | LP_SW_IE         | Write 1 to enable LP software interrupt. (R/W)                             |

### Description of Bits:
- **LP_SW_IE**: Write 1 to enable LP software interrupt. (R/W)
- **LP_UART_IE**: Write 1 to enable LP UART interrupt. (R/W)
- **LP_SPI_IE**: Write 1 to enable LP SPI interrupt. (R/W)
- **LP_I2C_IE**: Write 1 to enable I2C interrupt. (R/W)
- **LP_GPIO_IE**: Write 1 to enable LP GPIO interrupt. (R/W)
- **LP_ADC_IE**: Write 1 to enable LP ADC interrupt. (R/W)
- **LP_TOUCH_IE**: Write 1 to enable LP TOUCH interrupt. (R/W)
- **LP_TSENS_IE**: Write 1 to enable LP TSENS interrupt. (R/W)
- **LP_EFUSE_IE**: Write 1 to enable LP eFuse interrupt. (R/W)
- **LP_SYSREG_IE**: Write 1 to enable SYSREG interrupt. (R/W)
- **LP_ANAPERI_IE**: Write 1 to enable ANAPERI interrupt. (R/W)
- **LP_PMU_IE**: Write 1 to enable PMU interrupt. (R/W)
- **LP_MB_IE**: Write 1 to enable Mailbox interrupt. (R/W)
- **LP_TIMER_IE**: Write 1 to enable LP Timer interrupt. (R/W)
- **LP_WDT_IE**: Write 1 to enable WDT interrupt. (R/W)
- **LP_RTC_IE**: Write 1 to enable RTC interrupt. (R/W)
- **HP_IE**: Write 1 to enable HP interrupt. (R/W)

---

## Register 3.5. mtvec (0x305)

| Bit | Field Name       | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 31  | BASE             | Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W) |
|     |                  |                                                                             |
|     | MODE             | Represents whether machine mode interrupts are vectored. Only vectored mode `0x1` is available. (RO) |

- **BASE**: Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)
- **MODE**: Represents whether machine mode interrupts are vectored. Only vectored mode `0x1` is available. (RO)

```
Espressif Systems
```