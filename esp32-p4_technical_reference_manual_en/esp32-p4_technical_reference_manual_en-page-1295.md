

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.61. HP_SYSTEM_USBOTG20_CTRL_REG (0x015C)

Continued from the previous page...

HP_SYSTEM_SYS_PHY_PLL_FORCE_EN Configures whether or not to allow forcibly enabling USB OTG_HS PHY PLL by setting HP_SYSTEM_PHY_PLL_EN.
O: No effect
1: Force enable
(R/W)

HP_SYSTEM_SYS_PHY_PLL_EN Configures whether or not to enable USB OTG_HS PHY PLL. This setting is only valid when HP_SYSTEM_SYS_PHY_PLL_FORCE_EN is set.
O: No effect
1: Enable
(R/W)

HP_SYSTEM_SYS_OTG_PHY_BISTEN Configures whether or not to drive USB OTG_HS PHY into BIST mode and perform self-test.
O: No effect
1: In BIST mode
(R/W)

Register 20.62. HP_SYSTEM_HP_SPM_ERR_RESP_CTRL_REG (0x0160)
```
```markdown
31                                 0

[reserved]  HP_SYSTEM_HP_SPM_ERR_RESP_EN

0 O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O Reset

HP_SYSTEM_HP_SPM_ERR_RESP_EN Configures whether or not to report parity error to the HP CPU and trigger exception.
O: Disable
1: Enable
(R/W)
```