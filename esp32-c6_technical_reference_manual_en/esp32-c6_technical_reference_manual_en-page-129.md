

```markdown
| Register Value¹ | Wake-Up Source                  | Description                                                                                                                                                                                                 |
|-----------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1             | Register PMU_HP_TRIGGER_LP      | The HP CPU sets the register PMU_HP_TRIGGER_LP to wake up the LP CPU, and sets PMU_HP_SW_TRIGGER_INT_CLR to clear this wake-up source.                                                                      |
| 0x2             | LP UART                          | The LP UART receives a certain number of RX pulses. LPPERI_LP_UART_WAKEUP_EN needs to be enabled. For more information, please refer to Chapter 27 UART Controller (UART, LP_UART, UHCI). |
| 0x4             | LP IO                            | This wake-up source uses the LP IO interrupt status register signal. For more information, please refer to Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX).                                                         |
| 0x8             | ETM                              | Wake-up sources received from ETM can wake up the LP CPU. For more information, please refer to Chapter 11 Event Task Matrix (SOC_ETM).                                                                       |
| 0x10            | RTC timer                        | RTC timer target 1 timeout interrupt control. For more information, please refer to Chapter 12 Low-Power Management.                                                                                       |

¹ Value of the PMU_LP_CPU_WAKEUP_EN register

## 3.10 Register Summary
The addresses in this section are relative to Low-Power Peripheral base address provided in Table 5.3-2 in Chapter 5 System and Memory.

| Name                          | Description                     | Address   | Access |
|-------------------------------|----------------------------------|-----------|--------|
| LPPERI_CPU_REG                | LP CPU Control Register         | 0x000C    | R/W    |
| LPPERI_INTERRUPT_SOURCE_REG   | LP CPU Interrupt Status Register| 0x0020    | RO     |

## 3.11 Registers
The addresses in this section are relative to Low-Power Peripheral base address provided in Table 5.3-2 in Chapter 5 System and Memory.
```