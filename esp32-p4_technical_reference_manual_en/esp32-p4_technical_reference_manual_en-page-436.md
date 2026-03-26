

```markdown
## Register 6.15. DMA2D_OUT_ETM_CONF_CHn_REG (n: 0-3) (0x0068+0x100*n)

DMA2D_OUT_ETM_EN_CHn   Configures whether to enable the ETM function for TX channel n.
    0: Disable
    1: Enable
    (R/W)

DMA2D_OUT_ETM_LOOP_EN_CHn   Configures whether to use the ETM task to indicate the processing of the next descriptor for TX channel n.
    0: Not use ETM task
    1: Use ETM task
    (R/W)

DMA2D_OUT_DSCR_TASK_MAK_CHn   Configures the maximum number of tasks that can be cached for TX channel n. (R/W)
```

```markdown
## Register 6.16. DMA2D_OUT_DSCR_PORT_BLK_CHn_REG (n: 0-3) (0x006C+0x100*n)

DMA2D_OUT_DSCR_PORT_BLK_H_CHn   Configures the horizontal width of the basic unit for TX channel n in DSCR-PORT mode.
    Measurement unit: pixels. (R/W)

DMA2D_OUT_DSCR_PORT_BLK_V_CHn   Configures the vertical height of the basic unit for TX channel n in DSCR-PORT mode.
    Measurement unit: pixels. (R/W)
```