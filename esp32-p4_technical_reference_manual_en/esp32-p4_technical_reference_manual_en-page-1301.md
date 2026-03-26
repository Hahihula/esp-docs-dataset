

```markdown
Register 20.70. HP_SYSTEM_GPIO_O_HYS_CTRL0_REG (0x01C0)

31                                 0
+---------------------------------------------------------------+
| 0x000000 | Reset |
+---------------------------------------------------------------+

HP_SYSTEM_GPIO_O_HYS_LOW Configures whether or not to enable the hysteresis feature of HP GPIO16 ~ HP GPIO47.
0: No effect
1: Enable

See detailed information in Section 9.10 of Chapter 9 GPIO Matrix and IO MUX.
(R/W)

Register 20.71. HP_SYSTEM_GPIO_O_HYS_CTRL1_REG (0x01C4)

31                                 9   8                         0
+---------------------------------------------------------------+
| (reserved) | Ox0 | Reset |
+---------------------------------------------------------------+

HP_SYSTEM_GPIO_O_HYS_HIGH Configures whether or not to enable the hysteresis feature of HP GPIO48 ~ HP GPIO56.
0: No effect
1: Enable

See detailed information in Section 9.10 of Chapter 9 GPIO Matrix and IO MUX.
(R/W)
```