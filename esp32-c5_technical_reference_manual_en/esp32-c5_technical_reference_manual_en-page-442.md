

```markdown
Register 9.64. PCR_CPU_WAITI_CONF_REG (0x0114)

PCR_CPU_WAIT_MODE_FORCE_ON Configures whether or not to force on the gated CPU clock when CPU is in WFI (wait for interrupt) mode.
O: Not force enable
1: Force enable

Usually, after executing the WFI instruction, CPU enters the WFI mode, during which the gated CPU clock is turned off until any interrupts occur. In this way, power consumption is saved. If this bit is set, the gated CPU clock is always on and will not be turned off by the WFI instruction. (R/W)

PCR_CPU_WAITI_DELAY_NUM Configures the number of delay cycles to turn off the CPU clock after the CPU enters the WFI mode because of WFI instruction.
Measurement unit: CPU_CLK cycles.
(R/W)

Register 9.65. PCR_CPU_FREQ_CONF_REG (0x0118)

PCR_CPU_DIV_NUM Configures the divisor of HP_ROOT_CLK to generate CPU_CLK.
This field should be used together with PCR_AHB_DIV_NUM.
```