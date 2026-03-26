

```markdown
Register 19.82. PMS_PERI_REGIONm_LOW_REG (m: 2-7) (0x0024+0x8*(m-2))

PMS_PERI_REGIONm_LOW Configures the high 30 bits of the start address of peripheral register's regionm. (R/W)

Register 19.83. PMS_PERI_REGIONm_HIGH_REG (m: 2-7) (0x0028+0x8*(m-2))

PMS_PERI_REGIONm_HIGH Configures the high 30 bits of the end address of peripheral register's regionm. (R/W)

19.7.5 HP2LP_PERI_PMS_REG

The addresses in this section are relative to the H2LP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 19.84. PMS_HP2LP_PERI_PMS_DATE_REG (0x0000)

PMS_HP2LP_PERI_PMS_DATE Version control register (R/W)
```