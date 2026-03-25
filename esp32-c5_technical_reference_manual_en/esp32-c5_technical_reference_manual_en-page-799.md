

```markdown
HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG: When a timeout occurs, this register will record the master ID of the timeout.
```

### 19.3.4.2 HP Peripheral Timeout Protection Register

HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG configures the timeout protection for accessing HP peripherals, which refer to the peripherals or modules whose addresses are in the range of `0x6000_0000-0x6009_FFFF`. For details, please refer to Subsection 6.3.5 Modules/Peripherals Address Mapping in Chapter 6 System and Memory.

When a timeout occurs, the HP_PERI_TIMEOUT_INTR interrupt will be triggered.

*   `HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the master ID of the timeout.

### 19.3.4.3 LP Peripheral Timeout Protection Register

Register `LP_PERI_BUS_TIMEOUT_CONF_REG` configures the timeout protection for accessing LP peripherals, which refer to the peripherals or modules whose addresses are in the range of `0x600B_0000-0x600B_FFFF`. For details, please refer to Subsection 6.3.5 Modules/Peripherals Address Mapping in Chapter 6 System and Memory.

When a timeout occurs, the LP_PERI_TIMEOUT_INTR interrupt will be triggered.

*   `LP_PERI_BUS_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `LP_PERI_BUS_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `LP_PERI_BUS_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the master ID of the timeout.
```