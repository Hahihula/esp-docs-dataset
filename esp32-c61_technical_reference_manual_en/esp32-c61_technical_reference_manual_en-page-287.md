

```markdown
Chapter 6 GPIO Matrix and IO MUX

Register 6.15. GPIO_PINn_REG (n: 0-13, 22-29) (0x00D4+0x4*n)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 18  | GPIO_PINn_INT_ENA            |
| 17  | (reserved)                   |
| 16  | GPIO_PINn_WAKEUP_ENABLE      |
| 15  | GPIO_PINn_WD_INT_TYPE        |
| 14  | GPIO_PINn_SYNC2_BYPASS       |
| 13  | GPIO_PINn_PAD_DRIVER         |
| 12  | GPIO_PINn_SYNC1_BYPASS       |
| 11  | GPIO_PINn_INT_TYPE           |
| 10  | (reserved)                   |
| 9   | Reset                        |
| 8   | O                         |
| 7   | O                         |
| 6   | O                         |
| 5   | O                         |
| 4   | O                         |
| 3   | O                         |
| 2   | O                         |
| 1   | O                         |
| 0   | O                         |

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

GPIO_PINn_WAKEUP_ENABLE Configures whether or not to enable GPIO wakeup function.
- 0: Disable
- 1: Enable
    This function only wakes up the CPU from Light-sleep.
(R/W)

Continued on the next page...
```