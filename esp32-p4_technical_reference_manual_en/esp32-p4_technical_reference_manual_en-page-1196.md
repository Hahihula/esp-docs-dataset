

```markdown
Register 19.64. PMS_COREn_MM_HP_PERI_PMS_REG3_REG (n: 0-1) (0x0014+0x20*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
|     |                                             | (reserved)                                                                  |
| 5   | PMS_COREn_MM_HP_CLKRST_ALLOW               | Configures whether HP CPU in machine mode has permission to access HP_SYS_CLKRST. O: Not allowed<br>1: Allowed<br>(R/W) |
| 4   | PMS_COREn_MM_HP_SYS_REG_ALLOW              | Configures whether HP CPU in machine mode has permission to access HP system register.<br>O: Not allowed<br>1: Allowed<br>(R/W) |
| 3   | PMS_COREn_MM_HP_SYSTIMER_ALLOW             | Configures whether HP CPU in machine mode has permission to access HP system timer.<br>O: Not allowed<br>1: Allowed<br>(R/W) |
| 2   | PMS_COREn_MM_HP_IOMUX_ALLOW                | Configures whether HP CPU in machine mode has permission to access HP IO MUX.<br>O: Not allowed<br>1: Allowed<br>(R/W) |
| 1   | PMS_COREn_MM_HP_GPIO_ALLOW                 | Configures whether HP CPU in machine mode has permission to access HP GPIO Matrix.<br>O: Not allowed<br>1: Allowed<br>(R/W) |
| 0   |                                             | Reset                                                                       |
```