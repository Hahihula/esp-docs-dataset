

```markdown
Chapter 16 System Registers

0x600B_0000 ~ 0x600B_FFFF: For corresponding peripheral information, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the LP_PERI_TIMEOUT_INTR interrupt will be asserted.

*   `LP_PERI_BUS_TIMEOUT_CONF_REG`: Reserved.
*   `LP_PERI_BUS_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `LP_PERI_BUS_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the Master-ID of the timeout.

GoBack
```