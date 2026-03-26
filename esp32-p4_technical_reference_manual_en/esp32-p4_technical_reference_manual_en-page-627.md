

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.77. LP_GPIO_PINn_REG (n: 0 - 15) (0x0034+4*n)

LP_GPIO_PINn_WAKEUP_ENABLE Configures whether or not to enable GPIO wake-up function.
O: Disable
1: Enable
This function only wakes up system from Deep-sleep.
(R/W)

LP_GPIO_PINn_INT_TYPE Configures GPIO interrupt type.
O: GPIO interrupt disabled
1: Rising edge trigger
2: Falling edge trigger
3: Any edge trigger
4: Low level trigger
5: High level trigger
(R/W)

LP_GPIO_PINn_PAD_DRIVER Configures to select pin drive mode.
O: Normal output
1: Open drain output
(R/W)

LP_GPIO_PINn_EDGE_WAKEUP_CLR Configures to clear edge-triggered GPIO wake-up source in PMU.
1: The corresponding bit in LP_PMU_xxx will be cleared.
O: No effect.
(WT)
```