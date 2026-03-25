

```markdown
Register 12.15. SOC_ETM_CH_ENA_AD1_SET_REG (0x0010)

SOC_ETM_CH_ENABLEn (n: 32-49) Configures whether or not to enable channel n.
O: Invalid. No effect
1: Enable
(WT)
```

```markdown
Register 12.16. SOC_ETM_CH_ENA_AD1_CLR_REG (0x0014)

SOC_ETM_CH_DISABLEn (n: 32-49) Configures whether or not to disable channel n.
O: Invalid. No effect
1: Clear
(WT)
```

```markdown
Register 12.17. SOC_ETM_CHn_EVT_ID_REG (n: 0-49) (0x0018+0x8*n)

SOC_ETM_CHn_EVT_ID Configures channel n event ID. (R/W)
```