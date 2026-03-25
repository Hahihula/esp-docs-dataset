

```markdown
Register 19.5. HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG (0x000C)

HP_SYSTEM_CPU_PERI_TIMEOUT_THRES Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W)

HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR Write 1 to clear timeout interrupt. (WT)

HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN Configures whether to enable timeout protection for accessing CPU peripheral registers.
0: Disable
1: Enable
(R/W)
```

```markdown
Register 19.6. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR Represents the address information of abnormal access.
(RO)
```