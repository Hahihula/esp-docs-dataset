

```markdown
Chapter 20 System Registers (SYSREG)
GoBack

Register 20.81. HP_SYSTEM_ICM_INT_ENA_REG (0x0014)

31
+---------------------------------------------------------------+
| 3 | 2 | 1 | 0 |
| 0 | 0 | 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | Reset |
+---------------------------------------------------------------+

HP_SYSTEM_ICM_DLOCK_INT_ENA Write 1 to enable DLOCK_INT interrupt. (R/W)

HP_SYSTEM_ICM_SYS_ADDRHOLE_INT_ENA Write 1 to enable ICM_SYS_ADDRHOLE_INT interrupt. (R/W)

HP_SYSTEM_ICM_CPU_ADDRHOLE_INT_ENA Write 1 to enable ICM_CPU_ADDRHOLE_INT interrupt. (R/W)

Register 20.82. HP_SYSTEM_ICM_INT_CLR_REG (0x0018)

31
+---------------------------------------------------------------+
| 3 | 2 | 1 | 0 |
| 0 | 0 | 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+---------------------------------------------------------------+

HP_SYSTEM_ICM_DLOCK_INT_CLR Write 1 to clear DLOCK_INT interrupt. (WT)

HP_SYSTEM_ICM_SYS_ADDRHOLE_INT_CLR Write 1 to clear ICM_SYS_ADDRHOLE_INT interrupt. (WT)

HP_SYSTEM_ICM_CPU_ADDRHOLE_INT_CLR Write 1 to clear ICM_CPU_ADDRHOLE_INT interrupt. (WT)
```