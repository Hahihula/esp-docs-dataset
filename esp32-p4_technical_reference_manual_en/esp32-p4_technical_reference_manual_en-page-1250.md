

```markdown
LP CPU DBUS Timeout Protection

Configure LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_REG to enable timeout protection and set the timeout threshold for LP CPU accessing LPRAM and LP SPM by DBUS.

When a timeout occurs, the LP_CORE_DBUS_TIMEOUT_INTR interrupt will be asserted.

LP CPU AHB Bus Timeout Protection

Configure LP_SYSTEM_LP_CORE_AHB_TIMEOUT_REG to enable timeout protection and set the timeout threshold for LP CPU accessing LP peripherals, HP peripherals and CPU peripherals by AHB bus.

When a timeout occurs, the LP_CORE_AHB_TIMEOUT_INTR interrupt will be asserted.
```

```markdown
20.2.2.11 RNG Control

Registers LP_SYSTEM_RNG_DATA_REG and LP_SYSTEM_RNG_CFG_REG are used to configure and control the random number generator.
```

```markdown
20.3 Interrupt

ESP32-P4's System Registers can generate the following interrupt signal(s) that will be sent to the Interrupt Matrix.

*   HP_SYSREG_INTR
*   SYS_ICM_INTR
*   LP_SYSREG_INTR

There are several internal interrupt sources from System Registers that can generate the above interrupt signal(s). The interrupt sources from System Registers are listed with their trigger conditions and the resulted interrupt signal(s) in Table 20.3-1.
```

```markdown
Table 20.3-1. System Registers Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
| :------------------------ | :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------ |
| CPU_INT_FROM_CPU0         | Software interrupt. Triggered by writing 1 to HP_SYSTEM_HP_CPU_INT_FROM_CPU0_REG |                                        |
| CPU_INT_FROM_CPU1         | Software interrupt. Triggered by writing 1 to HP_SYSTEM_HP_CPU_INT_FROM_CPU1_REG |                                        |
| CPU_INT_FROM_CPU2         | Software interrupt. Triggered by writing 1 to HP_SYSTEM_HP_CPU_INT_FROM_CPU2_REG |                                        |
| CPU_INT_FROM_CPU3         | Software interrupt. Triggered by writing 1 to HP_SYSTEM_HP_CPU_INT_FROM_CPU3_REG |                                        |
| L2_MEM_ERR_RESP_INT       | Triggered when an error response occurs in L2MEM | HP_SYSREG_INTR |
| L2_MEM_EXCEED_ADDR_INT    | Triggered when L2MEM exceeds its address range |                  |
| L2_MEM_ECC_ERR_INT        | Triggered when a one-bit flip error is detected and corrected by ECC in L2MEM |                  |
| HP_SPM_PARITY_ERR_INT     | Triggered when a parity error occurs in HP SPM |                  |
```