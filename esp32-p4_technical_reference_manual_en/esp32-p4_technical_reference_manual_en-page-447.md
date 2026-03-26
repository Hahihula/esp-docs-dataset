

```markdown
Register 6.31. DMA2D_IN_ETM_CONF_CHn_REG (n: 0-2) (0x056C+0x100*n)
```

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 4   | DMA2D_IN_DSCR_TASK_MAK_CHn     | Configures the maximum number of tasks that can be cached for RX channel n. (R/W) |
| 3   | DMA2D_IN_ETM_LOOP_EN_CHn       | Configures whether to use the ETM task to indicate the processing of the next descriptor for RX channel n.<br>0: Not use ETM task<br>1: Use ETM task (R/W) |
| 2   | DMA2D_IN_ETM_EN_CHn            | Configures whether to enable the ETM function for RX channel n.<br>0: Disable<br>1: Enable (R/W) |
| 1   |                                | Reset                                                                       |
| 0   |                                | 0x1                                                                         |

DMA2D_IN_ETM_EN_CHn Configures whether to enable the ETM function for RX channel n.
- 0: Disable
- 1: Enable
(R/W)

DMA2D_IN_ETM_LOOP_EN_CHn Configures whether to use the ETM task to indicate the processing of the next descriptor for RX channel n.
- 0: Not use ETM task
- 1: Use ETM task
(R/W)

DMA2D_IN_DSCR_TASK_MAK_CHn Configures the maximum number of tasks that can be cached for RX channel n. (R/W)
```