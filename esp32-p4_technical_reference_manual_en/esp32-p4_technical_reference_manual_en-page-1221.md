

```markdown
Register 19.74. PMS_LP_MM_PMS_REG3_REG (0x011C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 5   | PMS_LP_MM_HP_CLKRST_ALLOW                                                  |
| 4   | PMS_LP_MM_HP_SYS_REG_ALLOW                                                 |
| 3   | PMS_LP_MM_HP_SYSTIMER_ALLOW                                                |
| 2   | PMS_LP_MM_HP_IOMUX_ALLOW                                                   |
| 1   | PMS_LP_MM_HP_GPIO_ALLOW                                                     |
| 0   | Reset                                                                       |

PMS_LP_MM_HP_GPIO_ALLOW Configures whether the LP CPU in machine mode has permission to access HP GPIO Matrix.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_IOMUX_ALLOW Configures whether the LP CPU in machine mode has permission to access HP IO MUX.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_SYSTIMER_ALLOW Configures whether the LP CPU in machine mode has permission to access HP system timer.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_SYS_REG_ALLOW Configures whether the LP CPU in machine mode has permission to access HP system register.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_CLKRST_ALLOW Configures whether the LP CPU in machine mode has permission to access HP_SYS_CLKRST.
O: Not allowed
1: Allowed
(R/W)
```

### 19.7.4 LP_PERI_PMS_REG

The addresses in this section are relative to the LP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```