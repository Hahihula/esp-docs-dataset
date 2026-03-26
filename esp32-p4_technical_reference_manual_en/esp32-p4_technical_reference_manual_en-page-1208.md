

```markdown
Register 19.68. PMS_COREn_UM_HP_PERI_PMS_REG3_REG (n: 0-1) (0x0024+0x20*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 5   | PMS_COREn_UM_HP_CLKRST_ALLOW                                               |
| 4   | PMS_COREn_UM_HP_SYS_REG_ALLOW                                               |
| 3   | PMS_COREn_UM_HP_SYSTEMER_ALLOW                                              |
| 2   | PMS_COREn_UM_HP_IOMUX_ALLOW                                                 |
| 1   | PMS_COREn_UM_HP_GPI0_ALLOW                                                  |
| 0   | Reset                                                                       |

PMS_COREn_UM_HP_GPI0_ALLOW Configures whether HP CPU in user mode has permission to access HP GPIO Matrix.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_IOMUX_ALLOW Configures whether HP CPU in user mode has permission to access HP IO MUX.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_SYSTEMER_ALLOW Configures whether HP CPU in user mode has permission to access HP system timer.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_SYS_REG_ALLOW Configures whether HP CPU in user mode has permission to access HP system register.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_CLKRST_ALLOW Configures whether HP CPU in user mode has permission to access HP_SYS_CLKRST.
O: Not allowed
1: Allowed
(R/W)
```

## 19.7.3 LP2HP_PERI_PMS_REG

The addresses in this section are relative to the LP2HP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```