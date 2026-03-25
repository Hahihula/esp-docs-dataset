

```markdown
Chapter 19 System Registers

Register 19.3. HP_SYSTEM_CORE_DEBUG_RUNSTALL_CONF_REG (0x0040)

HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE Configures whether to enable the RunStall feature for HP CPU and LP CPU, which means when any of the CPUs is in debug mode, the other one is stalled automatically.
O: Disable
1: Enable
(R/W)

HP_SYSTEM_CORE_RUNSTALLED Indicates the RunStall status of the HP CPU.
O: Not stalled
1: Stalled
(RO)
```