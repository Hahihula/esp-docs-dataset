

```markdown
Chapter 17 System Registers

0x6000_0000–0x6009_FFFF. For details, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the HP_PERI_TIMEOUT_INTR interrupt will be triggered. The related registers are:

*   `HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the master ID of the timeout.

17.3.3.3 LP Peripheral Timeout Protection Register

Register `LP_PERI_BUS_TIMEOUT_CONF_REG` configures the timeout protection for accessing LP peripherals, which refer to the peripherals or modules whose addresses are in the range of 0x600B_0000–0x600B_FFFF. For details, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the `LP_PERI_TIMEOUT_INTR` interrupt will be triggered. The related registers are:

*   `LP_PERI_BUS_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `LP_PERI_BUS_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `LP_PERI_BUS_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the master ID of the timeout.
```