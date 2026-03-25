

```markdown
Register 10.3. SOC_ETM_CH_ENA_ADO_CLR_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SOC_ETM_CH_DISABLE31 | SOC_ETM_CH_DISABLE30 | SOC_ETM_CH_DISABLE29 | SOC_ETM_CH_DISABLE28 | SOC_ETM_CH_DISABLE27 | SOC_ETM_CH_DISABLE26 | SOC_ETM_CH_DISABLE25 | SOC_ETM_CH_DISABLE24 | SOC_ETM_CH_DISABLE23 | SOC_ETM_CH_DISABLE22 | SOC_ETM_CH_DISABLE21 | SOC_ETM_CH_DISABLE20 | SOC_ETM_CH_DISABLE19 | SOC_ETM_CH_DISABLE18 | SOC_ETM_CH_DISABLE17 | SOC_ETM_CH_DISABLE16 | SOC_ETM_CH_DISABLE15 | SOC_ETM_CH_DISABLE14 | SOC_ETM_CH_DISABLE13 | SOC_ETM_CH_DISABLE12 | SOC_ETM_CH_DISABLE11 | SOC_ETM_CH_DISABLE10 | SOC_ETM_CH_DISABLE9 | SOC_ETM_CH_DISABLE8 | SOC_ETM_CH_DISABLE7 | SOC_ETM_CH_DISABLE6 | SOC_ETM_CH_DISABLE5 | SOC_ETM_CH_DISABLE4 | SOC_ETM_CH_DISABLE3 | SOC_ETM_CH_DISABLE2 | SOC_ETM_CH_DISABLE1 | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

SOC_ETM_CH_DISABLEn (n: 0-31) Configures whether to disable channel O.

O: Invalid. No effect
1: Disable
(WT)

Register 10.4. SOC_ETM_CH_ENA_AD1_REG (0x000C)

| Bit | 31 | reserved | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SOC_ETM_CH_ENABLED49 | SOC_ETM_CH_ENABLED48 | SOC_ETM_CH_ENABLED47 | SOC_ETM_CH_ENABLED46 | SOC_ETM_CH_ENABLED45 | SOC_ETM_CH_ENABLED44 | SOC_ETM_CH_ENABLED43 | SOC_ETM_CH_ENABLED42 | SOC_ETM_CH_ENABLED41 | SOC_ETM_CH_ENABLED40 | SOC_ETM_CH_ENABLED39 | SOC_ETM_CH_ENABLED38 | SOC_ETM_CH_ENABLED37 | SOC_ETM_CH_ENABLED36 | SOC_ETM_CH_ENABLED35 | SOC_ETM_CH_ENABLED34 | SOC_ETM_CH_ENABLED33 | SOC_ETM_CH_ENABLED32 | Reset |

SOC_ETM_CH_ENABLEDn (n: 32-49) Represents the status of channel n.

O: Disabled
1: Enabled
(R/WTC/SS)

Register 10.5. SOC_ETM_CH_ENA_AD1_SET_REG (0x0010)

| Bit | 31 | reserved | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SOC_ETM_CH_ENABLE49 | SOC_ETM_CH_ENABLE48 | SOC_ETM_CH_ENABLE47 | SOC_ETM_CH_ENABLE46 | SOC_ETM_CH_ENABLE45 | SOC_ETM_CH_ENABLE44 | SOC_ETM_CH_ENABLE43 | SOC_ETM_CH_ENABLE42 | SOC_ETM_CH_ENABLE41 | SOC_ETM_CH_ENABLE40 | SOC_ETM_CH_ENABLE39 | SOC_ETM_CH_ENABLE38 | SOC_ETM_CH_ENABLE37 | SOC_ETM_CH_ENABLE36 | SOC_ETM_CH_ENABLE35 | SOC_ETM_CH_ENABLE34 | SOC_ETM_CH_ENABLE33 | SOC_ETM_CH_ENABLE32 | Reset |

SOC_ETM_CH_ENABLEn (n: 32-49) Configures whether to enable channel n.

O: Invalid. No effect
1: Enable
(WT)
```