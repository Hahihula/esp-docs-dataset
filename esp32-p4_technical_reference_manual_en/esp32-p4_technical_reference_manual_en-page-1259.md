

```markdown
Chapter 20 System Registers (SYSREG)
GoBack

Register 20.8. HP_SYSTEM_HP_SPM_INT_ST_REG (0x0100)

HP_SYSTEM_HP_SPM_PARITY_ERR_INT_ST

31 30
+-----------------------------------------------+
| 0 | 0 | ... | 0 |
+-----------------------------------------------+
Reset

HP_SYSTEM_HP_SPM_PARITY_ERR_INT_ST The masked interrupt status of HP_SPM_PARITY_ERR_INT interrupt. (RO)

Register 20.9. HP_SYSTEM_HP_SPM_INT_ENA_REG (0x0104)

HP_SYSTEM_HP_SPM_PARITY_ERR_INT_ENA

31 30
+-----------------------------------------------+
| 0 | 0 | ... | 0 |
+-----------------------------------------------+
Reset

HP_SYSTEM_HP_SPM_PARITY_ERR_INT_ENA Write 1 to enable HP_SPM_PARITY_ERR_INT interrupt. (R/W)
```