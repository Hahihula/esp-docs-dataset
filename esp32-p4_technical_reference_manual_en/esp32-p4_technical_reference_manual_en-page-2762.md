

```markdown
Register 54.25. SDHOST_DLL_CLK_CONF_REG (0x0808)
```

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 21 | 20 | (reserved) | 15 | 14 | SDHOST_DLL_CCLK_IN_SAM_PHASE | 9 | 8 | SDHOST_DLL_CCLK_IN_DRV_PHASE | 3 | 2 | SDHOST_DLL_CCLK_IN_SLF_PHASE | 0 | Reset |

SDHOST_DLL_CCLK_IN_SLF_PHASE Configures the clock phase of the internal signal when selecting high frequency clock. Unit is 1/64 of clock cycle. (R/W)

SDHOST_DLL_CCLK_IN_DRV_PHASE Configures the clock phase of the output signal when selecting high frequency clock. Unit is 1/64 of clock cycle. (R/W)

SDHOST_DLL_CCLK_IN_SAM_PHASE Configures the clock phase of the input signal when selecting high frequency clock. Unit is 1/64 of clock cycle. (R/W)
```