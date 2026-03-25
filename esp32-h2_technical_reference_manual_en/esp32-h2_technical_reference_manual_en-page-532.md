

```markdown
Chapter 16 System Registers

GoBack

By default, the field HP_SYSTEM_SEC_DPA_CFG_SEL in register HP_SYSTEM_SEC_DPA_CONF_REG is 0. In this case, the security-level is decided by the eFuse field EFUSE_SEC_DPA_LEVEL. If the field HP_SYSTEM_SEC_DPA_CFG_SEL is set to 1, the security-level is decided by HP_SYSTEM_SEC_DPA_CFG_LEVEL in register HP_SYSTEM_SEC_DPA_CONF_REG.

16.2.3 Bus Timeout Protection

The Bus Timeout Protection function can be enabled and the timeout threshold can be configured through the configuration register. When a transfer is initiated, the counter inside the Timeout Protection module will increase by one every clock cycle. When the accumulated value is less than the timeout threshold and the bus receives a response from the slave, the internal counter is cleared. When the accumulated value is greater than the timeout threshold, if the slave device has not responded to the transfer, the Timeout Protection module will force the bus return signal to be pulled high. At the same time, it will report the interrupt and record the abnormal access address and master ID.

16.2.3.1 CPU Peripheral Timeout Protection Register

HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG is the timeout protection configuration register for accessing CPU peripheral registers. CPU peripherals refer to the peripherals or modules whose addresses are in the range of 0x600C_0000 ~ 0x600C_FFFF. For corresponding peripheral information, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the CPU_PERI_TIMEOUT_INTR interrupt will be asserted.
* HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG: Reserved.
* HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG: When a timeout occurs, this register will record the address of the timeout.
* HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG: When a timeout occurs, this register will record the Master-ID of the timeout.

16.2.3.2 HP Peripheral Timeout Protection Register

HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG is the timeout protection configuration register for accessing HP peripheral registers. HP peripherals refer to the peripherals or modules whose addresses are in the range of 0x6000_0000 ~ 0x6009_FFFF. For corresponding peripheral information, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the HP_PERI_TIMEOUT_INTR interrupt will be asserted.
* HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG: Reserved.
* HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG: When a timeout occurs, this register will record the address of the timeout.
* HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG: When a timeout occurs, this register will record the Master-ID of the timeout.

16.2.3.3 LP Peripheral Timeout Protection Register

LP_PERI_BUS_TIMEOUT_CONF_REG is the timeout protection configuration register for accessing LP peripheral registers. LP peripherals refer to the peripherals or modules whose addresses are in the range of
```