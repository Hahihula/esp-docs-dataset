

```markdown
Register 13.17. SOC_ETM_TASK_ST6_REG (0x0218)

Continued from the previous page...

SOC_ETM_DMA2D_TASK_OUT_DSCR_READY_CH1_ST   Represents     the      status      of
DMA2D_TASK_OUT_DSCR_READY_CH1.
O: Not generated
1: Generated
(R/WTC/SS)

SOC_ETM_DMA2D_TASK_OUT_DSCR_READY_CH2_ST   Represents     the      status      of
DMA2D_TASK_OUT_DSCR_READY_CH2.
O: Not generated
1: Generated
(R/WTC/SS)


Register 13.18. SOC_ETM_CH_ENA_ADO_SET_REG (0x0004)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SOC_ETM_CH_ENABLEn (n: 0-31) Configures whether to enable channeln.
O: Invalid. No effect
1: Enable
(WT)
```