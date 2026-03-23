

```markdown
Chapter 17 System Registers



GoBack


17.3.4.2 HP Peripheral Timeout Protection Register

HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG is the timeout protection configuration register for accessing HP peripheral registers.

HP peripherals refer to the peripherals or modules whose addresses are in the range of 0x6000_0000 ~ 0x6009_FFFF. For corresponding peripheral information, please refer to Subsection 5.3.5 Modules/Peripherals Address Mapping in Chapter 5 System and Memory.

When a timeout occurs, the HP_PERI_TIMEOUT_INTR interrupt will be asserted.

*   `HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the Master-ID of the timeout.



17.3.4.3 LP Peripheral Timeout Protection Register

LP_PERI_BUS_TIMEOUT_CONF_REG is the timeout protection configuration register for accessing LP peripheral registers. LP peripherals refer to the peripherals or modules whose addresses are in the range of 0x600B_0000 ~ 0x600B_FFFF. For corresponding peripheral information, please refer to Subsection 5.3.5 Modules/Peripherals Address Mapping in Chapter 5 System and Memory.

When a timeout occurs, the LP_PERI_TIMEOUT_INTR interrupt will be asserted.

*   `LP_PERI_BUS_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `LP_PERI_BUS_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `LP_PERI_BUS_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the Master-ID of the timeout.
```