

```markdown
Chapter 20 System Registers (SYSREG)
GoBack

Register 20.43. HP_SYSTEM_HP_CPU_WAITI_CONF_REG (0x0118)

HP_SYSTEM_CPU_WAIT_MODE_FORCE_ON Configures whether or not to force on cpu_waiti_clk.
(R/W)

HP_SYSTEM_CPU_WAITI_DELAY_NUM Configures the delay cycles when CPU enters wait mode;
after the configured delay, cpu_waiti_clk turns off. (R/W)

Register 20.44. HP_SYSTEM_CORE_DEBUG_RUNSTALL_CONF_REG (0x011C)

HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE Configures whether or not to enable debug run-
stall feature between HP CPU and LP CPU.
O: Disable
1: Enable
(R/W)
```