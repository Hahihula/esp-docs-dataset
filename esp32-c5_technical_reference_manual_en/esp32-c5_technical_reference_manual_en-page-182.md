

```markdown
| Register Value¹ | Wake-Up Source                  | Description                                                                                                                                                                                                 |
|-----------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1             | Register PMU_HP_TRIGGER_LP      | The HP CPU sets the register PMU_HP_TRIGGER_LP to wake up the LP CPU, and sets PMU_HP_SW_TRIGGER_INT_CLR to clear this wake-up source.                                                                        |
| 0x2             | LP UART                          | The LP UART receives a certain number of RX pulses. LPPERI_LP_UART_WAKEUP_EN needs to be enabled. For more information, please refer to Chapter 32 UART Controller (UART).                                                        |
| 0x4             | LP IO                            | This wake-up source uses the LP IO interrupt status register signal. For more information, please refer to Chapter 8 GPIO Matrix and IO MUX.                                                                         |
| 0x8             | ETM                              | Wake-up sources received from ETM can wake up the LP CPU. For more information, please refer to Chapter 12 Event Task Matrix (ETM).                                                                               |
| 0x10            | RTC timer                       | RTC timer target 1 timeout interrupt control. For more information, please refer to Chapter 13 Low-Power Management.                                                                                           |

¹ Value of the PMU_LP_CPU_WAKEUP_EN register
```

## 4.10 Register Summary

The addresses in this section are relative to Low-Power Peripheral base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                 | Description                     | Address | Access |
|--------------------------------------|----------------------------------|---------|--------|
| LPPERI_CPU_REG                       | LP CPU Control Register         | 0x000C  | R/W    |
| LPPERI_INTERRUPT_SOURCE_REG          | LP CPU Interrupt Status Register| 0x0020  | RO     |

## 4.11 Registers

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

The addresses in this section are relative to Low-Power Peripheral base address provided in Table 6.3-2 in Chapter 6 System and Memory.
```