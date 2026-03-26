

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.64. HP_SYSTEM_HP_SPM_INIT_REG (0x0168)

HP_SYSTEM_HP_SPM_INIT_EN Configures whether or not to enable HP SPM parity bit initialization.
O: Disable
1: Enable
(R/W)

HP_SYSTEM_HP_SPM_INIT_CNT_RESET Configures whether or not to reset TCM initialization count.
O: No effect
1: Reset
(R/W)

HP_SYSTEM_HP_SPM_INIT_DONE Represents the initialization status of HP SPM parity bits. (RO)

Register 20.65. HP_SYSTEM_HP_SPM_PARITY_CHECK_CTRL_REG (0x016C)

HP_SYSTEM_HP_SPM_PARITY_CHECK_EN Configures whether or not to enable parity error check in HP SPM.
O: Disable
1: Enable
(R/W)
```