

```markdown
Register 9.28. GPIO_PINn_REG (n: 0 - 54) (0x0074+0x4*n)

| 31 | 18 | 17 | 13 | 12 | 11 | 10 | 9 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0x0| 0x0| 0x0| 0x0| Reset |

GPIO_PINn_SYNC2_BYPASS Configures whether or not to synchronize GPIO input data on either edge of HP IO MUX operating clock for the second-level synchronization.
- 0: Not synchronize
- 1: Synchronize on falling edge
- 2: Synchronize on rising edge
- 3: Synchronize on rising edge (R/W)

GPIO_PINn_PAD_DRIVER Configures to select pin drive mode.
- 0: Normal output
- 1: Open drain output (R/W)

GPIO_PINn_SYNC1_BYPASS Configures whether or not to synchronize GPIO input data on either edge of HP IO MUX operating clock for the first-level synchronization.
- 0: Not synchronize
- 1: Synchronize on falling edge
- 2: Synchronize on rising edge
- 3: Synchronize on rising edge (R/W)

GPIO_PINn_INT_TYPE Configures GPIO interrupt type.
- 0: GPIO interrupt disabled
- 1: Rising edge trigger
- 2: Falling edge trigger
- 3: Any edge trigger
- 4: Low level trigger
- 5: High level trigger (R/W)

GPIO_PINn_WAKEUP_ENABLE Configures whether or not to enable GPIO wake-up function.
- 0: Disable
- 1: Enable
    This function only wakes up the CPU from Light-sleep.
(R/W)
```
Continued on the next page...
```