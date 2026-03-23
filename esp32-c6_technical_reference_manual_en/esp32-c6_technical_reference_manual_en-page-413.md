

```markdown
Register 11.3. SOC_ETM_CH_ENA_ADO_CLR_REG (0x0008)

SOC_ETM_CH_DISABLEn (n: 0-31) Configures whether to disable channel O.

O: Invalid. No effect
1: Disable
(WT)
```

```markdown
Register 11.4. SOC_ETM_CH_ENA_AD1_REG (0x000C)

SOC_ETM_CH_ENABLEDn (n: 32-49) Represents the status of channel n.

O: Disabled
1: Enabled
(R/WTC/SS)
```

```markdown
Register 11.5. SOC_ETM_CH_ENA_AD1_SET_REG (0x0010)

SOC_ETM_CH_ENABLEn (n: 32-49) Configures whether to enable channel n.

O: Invalid. No effect
1: Enable
(WT)
```