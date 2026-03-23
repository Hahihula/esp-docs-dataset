

```markdown
Register 7.13. GPIO_PINn_REG (n: 0-30) (0x0074+4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 18  | GPIO_PINn_INT_ENA                                                           |
| 17  | (reserved)                                                                  |
| 13  | GPIO_PINn_WAKEUP_ENABLE                                                    |
| 12  | GPIO_PINn_INT_TYPE                                                          |
| 11  | GPIO_PINn_SYNC1_BYPASS                                                     |
| 10  | GPIO_PINn_PAD_DRIVER                                                       |
| 9   | GPIO_PINn_SYNC2_BYPASS                                                     |
| 6-4 | (reserved)                                                                  |
| 3   | Reset                                                                      |
| 2   | 0x0                                                                        |
| 1   | 0x0                                                                        |
| 0   | 0x0                                                                        |

GPIO_PINn_SYNC2_BYPASS Configures whether or not to synchronize GPIO input data on either edge of IO MUX operating clock for the second-level synchronization.
- 0: Not synchronize
- 1: Synchronize on falling edge
- 2: Synchronize on rising edge
- 3: Synchronize on rising edge (R/W)

GPIO_PINn_PAD_DRIVER Configures to select pin drive mode.
- 0: Normal output
- 1: Open drain output (R/W)

GPIO_PINn_SYNC1_BYPASS Configures whether or not to synchronize GPIO input data on either edge of IO MUX operating clock for the first-level synchronization.
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