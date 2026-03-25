

```markdown
Register 16.5. HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG (0x0014)

HP_SYSTEM_CPU_PERI_TIMEOUT_UID Represents the master id[4:0] and master permission[6:5]
when trigger timeout. This register will be cleared after the interrupt is cleared. (WTC)


Register 16.6. HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG (0x0018)

HP_SYSTEM_HP_PERI_TIMEOUT_THRES Configures the timeout threshold for bus access for ac-
cessing HP peripheral register, corresponding to the number of clock cycles of the clock do-
main. (R/W)

HP_SYSTEM_HP_PERI_TIMEOUT_INT_CLEAR Configures whether or not to clear timeout interrupt.
0: No effect
1: Clear timeout interrupt
(WT)

HP_SYSTEM_HP_PERI_TIMEOUT_PROTECT_EN Configures whether or not to enable timeout pro-
tection for accessing HP peripheral registers.
0: Disable
1: Enable
(R/W)
```