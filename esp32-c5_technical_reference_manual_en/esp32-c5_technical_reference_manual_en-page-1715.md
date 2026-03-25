

```markdown
## 46.10 Registers

The addresses in this section are relative to SAR ADC Controller base address provided in Table 6.3-2 in Chapter 6 System and Memory.

### Register 46.1. APB_SARADC_CTRL_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    | (reserved) | APB_SARADC_XPD_SAR_FORCE | (reserved) | APB_SARADC_SAR_PATT_P_CLEAR | (reserved) | APB_SARADC_SAR_PATT_LEN | (reserved) | APB_SARADC_SAR_CLK_GATED | (reserved) | APB_SARADC_START_FORCE | APB_SARADC_START |
|     |    |    |             |                          |              |                         |               |                       |                        |                  |                     |                    |

```
0 0 0 0 0 0 0 0 0 0 7 4 1 0 0 0 0 0 0 Reset

---

**APB_SARADC_START_FORCE** Configures whether to use software to enable SAR ADC.
- 0: Select FSM to start SAR ADC
- 1: Select software to start SAR ADC
(R/W)

**APB_SARADC_START** Configures whether to start SAR ADC by software.
- 0: No effect
- 1: Start SAR ADC by software
Valid only when `APB_SARADC_START_FORCE = 1`.
(R/W)

**APB_SARADC_SAR_CLK_GATED** Configures whether to enable SAR ADC clock gate.
- 0: Disable
- 1: Enable
(R/W)

**APB_SARADC_SAR_PATT_LEN** Configures how many patterns will be used.
- 0: Use only cmd0
- 1: Use cmd0 and cmd1
- n: Use cmd0 to cmdn, the maximum n is 7
(R/W)

**APB_SARADC_SAR_PATT_P_CLEAR** Configures whether to clear the pointer of pattern table for DIG ADC controller.
- 0: No effect
- 1: Clear
(R/W)

**APB_SARADC_XPD_SAR_FORCE** Configures whether to forcibly power up SAR ADC.
- 0: No effect
- 1: Forcibly power up SAR ADC
(R/W)
```