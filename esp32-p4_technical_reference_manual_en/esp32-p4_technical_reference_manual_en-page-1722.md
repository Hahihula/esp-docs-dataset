

```markdown
## Chapter 36 Image Signal Processor (ISP)

### Register 36.104. ISP_SHADOW_REG_CTRL_REG (0x0270)
| 31 | 30 | 29 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|-----|---|---|---|---|---|---|---|---|---|
| 0x1| O | O | O | O | O | O | O | O | O | O | O | Reset |

- ISP_BLC_UPDATE Write 1 to update the BLC registers. (R/W)
- ISP_DPC_UPDATE Write 1 to update the DPC registers. (R/W)
- ISP_BF_UPDATE Write 1 to update the BF registers. (R/W)
- ISP_WBG_UPDATE Write 1 to update the WBG registers. (R/W)
- ISP_CCM_UPDATE Write 1 to update the CCM registers. (R/W)
- ISP_SHARP_UPDATE Write 1 to update the SHARP registers. (R/W)
- ISP_COLOR_UPDATE Write 1 to update the COLOR registers. (R/W)

ISP_SHADOW_UPDATE_SEL Configures the shadow register update mode.
0: Disable shadow registers
1: Automatically update at every vsync
2: After writing 1 to the corresponding update register, automatically update at the next vsync (R/W)
```

### Register 36.105. ISP_DPC_DEADPIX_CNT_REG (0x0044)

| 31 | ... | 10 | 9 | ... | 0 |
|----|-----|----|---|-----|---|
| O | O | O | O | Ox0 | Reset |

ISP_DPC_DEADPIX_CNT Represents the number of dead pixels counted during static calibration. (RO)
```