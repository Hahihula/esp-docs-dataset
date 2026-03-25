

```markdown
Chapter 17 System Registers

Register 17.5. HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG (0x0014)

HP_SYSTEM_CPU_PERI_TIMEOUT_UID Represents the master ID[4:0] and master permission[6:5]
when trigger timeout. For details, see Chapter 16 Permission Control (PMS). This register will be
cleared after the interrupt is cleared. (WTC)

Register 17.6. HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG (0x0018)

HP_SYSTEM_HP_PERI_TIMEOUT_THRES Configures the timeout threshold for bus access for ac-
cessing HP peripheral registers, corresponding to the number of clock cycles of the clock do-
main. (R/W)

HP_SYSTEM_HP_PERI_TIMEOUT_INT_CLEAR Write 1 to clear timeout interrupt.(WT)

HP_SYSTEM_HP_PERI_TIMEOUT_PROTECT_EN Configures whether to enable timeout protection
for accessing HP peripheral registers.
0: Disable
1: Enable
(R/W)
```