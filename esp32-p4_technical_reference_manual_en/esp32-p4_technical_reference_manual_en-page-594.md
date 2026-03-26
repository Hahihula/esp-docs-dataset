

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.28. GPIO_PINn_REG (n: 0 - 54) (0x0074+0x4*n)

Continued from the previous page...

GPIO_PINn_INT_ENA Configures whether or not to enable CPU interrupt or CPU non-maskable interrupt.

bit13: Configures whether or not to enable CPU interrupt 0:
O: Disable
1: Enable

bit14: Configures whether or not to enable CPU interrupt 1:
O: Disable
1: Enable

bit15: invalid

bit16: Configures whether or not to enable CPU interrupt 2:
O: Disable
1: Enable

bit17: Configures whether or not to enable CPU interrupt 3:
O: Disable
1: Enable

(R/W)
```