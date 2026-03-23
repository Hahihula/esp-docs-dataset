

```markdown
Register 7.45. LP_IO_PINn_REG (n: 0-7) (0x0028+0x4*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 11  | LP_GPIO_PINn_WAKEUP_ENABLE               | Configures whether or not to enable GPIO n wake-up function.                |
| 10  | LP_GPIO_PINn_EDGE_WAKEUP_CLR             | Configures whether or not to clear the edge wake-up status of GPIO n.        |
| 7   | LP_GPIO_PINn_INT_TYPE                    | Configures GPIO n interrupt type.                                          |
| 6   | (reserved)                               |                                                                             |
| 4   | LP_GPIO_PINn_PAD_DRIVER                  | Configures to select the pin drive mode of GPIO n.                          |
| 3   | LP_GPIO_PINn_WAKEUP_ENABLE               | Enables wake-up function for GPIO n.                                        |
| 2   | LP_GPIO_PINn_EDGE_WAKEUP_CLR             | Clears edge wake-up status if written 1.                                     |
| 1   | (reserved)                               |                                                                             |
| 0   | Reset                                    |                                                                             |

LP_GPIO_PINn_PAD_DRIVER Configures to select the pin drive mode of GPIO n.
- 0: Normal output
- 1: Open drain output
(R/W)

LP_GPIO_PINn_EDGE_WAKEUP_CLR Configures whether or not to clear the edge wake-up status of GPIO0 ~ GPIO7.
- bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
- If the value 1 is written to a bit here, the edge wake-up status of corresponding GPIO will be cleared.
(WT)

LP_GPIO_PINn_INT_TYPE Configures GPIO n interrupt type.
- 0: GPIO interrupt disabled
- 1: Rising edge trigger
- 2: Falling edge trigger
- 3: Any edge trigger
- 4: Low level trigger
- 5: High level trigger
(R/W)

LP_GPIO_PINn_WAKEUP_ENABLE Configures whether or not to enable GPIO n wake-up function.
- 0: Not enable
- 1: Enable
This function is disabled when PD_LP_PERI is powered off.
(R/W)
```