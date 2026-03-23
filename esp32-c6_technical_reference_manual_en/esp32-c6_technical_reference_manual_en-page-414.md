

```markdown
Register 11.6. SOC_ETM_CH_ENA_AD1_CLR_REG (0x0014)

SOC_ETM_CHn_DISABLEn (n: 32-49) Configures whether to disable channeln.
O: Invalid. No effect
1: Disable
(WT)

Register 11.7. SOC_ETM_Ch_n_EVT_ID_REG (n: 0-49) (0x0018+0x8*n)

SOC_ETM_Ch_n_EVT_ID (n: 0-49) Configures the event ID of channeln. See Table 11.3-1. (R/W)

Register 11.8. SOC_ETM_Ch_n_TASK_ID_REG (n: 0-49) (0x001C+0x8*n)

SOC_ETM_Ch_n_TASK_ID (n: 0-49) Configures the task ID of channeln. See Table 11.3-2. (R/W)
```