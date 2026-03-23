

```markdown
Register 5.14. GPIO_PINn_REG (n: 0-21) (0x0074+4*n)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                                                  |
| 18        | GPIO_PINn_SYNC2_BYPASS                                                     |
| 17        | GPIO_PINn_PAD_DRIVER                                                       |
| 16        | GPIO_PINn_SYNC1_BYPASS                                                     |
| 15        | GPIO_PINn_INT_TYPE                                                         |
| 14        | GPIO_PINn_WAKEUP_ENABLE                                                   |
| 13        | GPIO_PINn_CONFIG                                                            |
| 12        | GPIO_PINn_INT_ENA                                                          |

GPIO_PINn_SYNC2_BYPASS For the second stage synchronization, GPIO input data can be synchronized on either edge of the APB clock. O: no synchronization; 1: synchronized on falling edge; 2 and 3: synchronized on rising edge. (R/W)

GPIO_PINn_PAD_DRIVER pin drive selection. O: normal output; 1: open drain output. (R/W)

GPIO_PINn_SYNC1_BYPASS For the first stage synchronization, GPIO input data can be synchronized on either edge of the APB clock. O: no synchronization; 1: synchronized on falling edge; 2 and 3: synchronized on rising edge. (R/W)

GPIO_PINn_INT_TYPE Interrupt type selection. O: GPIO interrupt disabled; 1: rising edge trigger; 2: falling edge trigger; 3: any edge trigger; 4: low level trigger; 5: high level trigger. (R/W)

GPIO_PINn_WAKEUP_ENABLE GPIO wake-up enable bit, only wakes up the CPU from Light-sleep. (R/W)

GPIO_PINn_CONFIG reserved (R/W)

GPIO_PINn_INT_ENA Interrupt enable bits. bit13: CPU interrupt enabled; bit14: CPU non-maskable interrupt enabled. (R/W)
```

```markdown
Register 5.15. GPIO_STATUS_NEXT_REG (0x014C)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                                                  |
| 26-25     | GPIO_STATUS_INTERRUPT_NEXT                                                 |

GPIO_STATUS_INTERRUPT_NEXT Interrupt source signal of GPIO0 ~ 21, could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. (RO)
```