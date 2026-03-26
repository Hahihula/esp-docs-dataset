

```markdown
Register 20.61. HP_SYSTEM_USBOTG20_CTRL_REG (0x015C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|-------------|--------------------------|-----------------------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
|     |    |    |    |    |    |    | (reserved)   | HP_SYSTEM_SYS_OTG_PHY_BIST_EN | (reserved)                                     | HP_SYSTEM_SYS_PHY_BIST_EN                         | HP_SYSTEM_SYS_PHY_PL_PL_EN | HP_SYSTEM_SYS_PHY_RTN | HP_SYSTEM_SYS_PHY_SUSPEND_FORCE_EN | HP_SYSTEM_SYS_PHY_SUSPEND_FORCE_EN | HP_SYSTEM_SYS_OTG_PHY_TEST_DONE |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0            | 0                         | 0                                              | 1                                                | 0                          | 0                    | 0                                      | (reserved)                           |

HP_SYSTEM_SYS_OTG_PHY_TEST_DONE Indicates the status of USB OTG_HS PHY BIST test.
O: Fail
1: Pass
(RO)

HP_SYSTEM_SYS_PHY_SUSPENDM Configures whether or not to drive USB OTG_HS PHY into Suspend mode. This setting is only valid when HP_SYSTEM_PHY_SUSPEND_FORCE_EN is set to 1.
O: No effect
1: In Suspend mode
(R/W)

HP_SYSTEM_SYS_PHY_SUSPEND_FORCE_EN Configures whether or not to allow forcing USB OTG_HS PHY into Suspend mode by setting HP_SYSTEM_PHY_SUSPENDM.
O: No effect
1: Force in Suspend mode
(R/W)

HP_SYSTEM_SYS_PHY_RSTN Configures whether or not to reset USB OTG_HS PHY. This setting is only valid when HP_SYSTEM_PHY_RESET_FORCE_EN is set to 1.
O: Reset
1: No effect
(R/W)

HP_SYSTEM_SYS_PHY_RESET_FORCE_EN Configures whether or not to allow forcibly resetting USB OTG_HS PHY by clearing HP_SYSTEM_PHY_RSTN.
O: No effect
1: Force reset
(R/W)
```