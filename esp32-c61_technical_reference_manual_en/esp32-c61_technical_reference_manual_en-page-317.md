

```markdown
Register 6.51. LP_GPIO_PINn_REG (n: 0-6) (0x0030+0x4*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | LP_GPIO_PINn_WAKEUP_ENABLE               |                                                                             |
| 29  | LP_GPIO_PINn_INT_TYPE                    | Configures GPIO interrupt type.                                             |
|     |                                          | 0: GPIO interrupt disabled<br>1: Rising edge trigger<br>2: Falling edge trigger<br>3: Any edge trigger<br>4: Low level trigger<br>5: High level trigger (R/W) |
| 28  | LP_GPIO_PINn_EDGE_WAKEUP_CLR             | Configures whether or not to clear the edge wake-up status of GPIO0~GPIO6.<br>0: No effect<br>1: Clear (WT) |
| 27  | LP_GPIO_PINn_SYNC2_BYPASS                | Configures whether or not to synchronize GPIO input data on either edge of LP IO MUX operating clock for the second-level synchronization.<br>0: Not synchronize<br>1: Synchronize on falling edge<br>2: Synchronize on rising edge<br>3: Synchronize on rising edge (R/W) |
| 26  | LP_GPIO_PINn_PAD_DRIVER                  | Configures to select the pin drive mode of GPIO n.<br>0: Normal output<br>1: Open drain output (R/W) |
| 25  | LP_GPIO_PINn_SYNC1_BYPASS                | Configures whether or not to synchronize GPIO input data on either edge of LP IO MUX operating clock for the first-level synchronization.<br>0: Not synchronize<br>1: Synchronize on falling edge<br>2: Synchronize on rising edge<br>3: Synchronize on rising edge (R/W) |
```

Continued on the next page...
```