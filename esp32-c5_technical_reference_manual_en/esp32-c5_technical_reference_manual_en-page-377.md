

```markdown
Register 8.54. LP_GPIO_PINn_REG (n: 0-6) (0x0030+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_GPIO_PINn_WAKEUP_ENABLE                                               |
| 29  | LP_GPIO_PINn_INT_TYPE                                                     |
| 28  | (reserved)                                                                |
| 27  | LP_GPIO_PINn_SYNC2_BYPASS                                                |
| 26  | LP_GPIO_PINn_PAD_DRIVER                                                  |
| 25  | LP_GPIO_PINn_SYNC1_BYPASS                                                |
| 24  | LP_GPIO_PINn_EDGE_WAKEUP_CLR                                             |
| 0   | Reset                                                                     |

LP_GPIO_PINn_SYNC2_BYPASS Configures whether or not to synchronize GPIO input data on either edge of LP IO MUX operating clock for the second-level synchronization.
- O: Not synchronize
- 1: Synchronize on falling edge
- 2: Synchronize on rising edge
- 3: Synchronize on rising edge (R/W)

LP_GPIO_PINn_PAD_DRIVER Configures to select the pin drive mode of GPIO n.
- O: Normal output
- 1: Open drain output (R/W)

LP_GPIO_PINn_SYNC1_BYPASS Configures whether or not to synchronize GPIO input data on either edge of LP IO MUX operating clock for the first-level synchronization.
- O: Not synchronize
- 1: Synchronize on falling edge
- 2: Synchronize on rising edge
- 3: Synchronize on rising edge (R/W)

LP_GPIO_PINn_EDGE_WAKEUP_CLR Configures whether or not to clear the edge wake-up status of GPIO0~GPIO6.
- O: No effect
- 1: Clear (WT)

LP_GPIO_PINn_INT_TYPE Configures GPIO n interrupt type.
- O: GPIO interrupt disabled
- 1: Rising edge trigger
- 2: Falling edge trigger
- 3: Any edge trigger
- 4: Low level trigger
- 5: High level trigger (R/W)
```