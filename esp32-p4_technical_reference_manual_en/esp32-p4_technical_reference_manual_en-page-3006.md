

```markdown
Register 60.24. LP_ANA_TOUCH_FREQn_SCAN_PARA_REG (n: 0~2) (0x012C+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_ANA_TOUCH_FREQn_DBIAS                                                    |
| 29  | LP_ANA_TOUCH_FREQn_DRV_HS                                                  |
| 28  | LP_ANA_TOUCH_FREQn_DRV_LS                                                  |
| 27  | LP_ANA_TOUCH_FREQn_DCAP_LPF                                                |
| 26  | LP_ANA_TOUCH_FREQn_DRES_LPF                                                |
| 25  | Reset                                                                      |

LP_ANA_TOUCH_FREQn_DCAP_LPF Configures the touch sensor low-pass filter for sampling frequency mode n. The adjustment range is 0-2.54 pF, and the step is 20 fF. (R/W)(R/W)

LP_ANA_TOUCH_FREQn_DRES_LPF Configures the touch sensor low-pass filter for sampling frequency mode n.

0: 0 kΩ
1: 3 kΩ
2: 4.5 kΩ
3: 7.5 kΩ
(R/W)

LP_ANA_TOUCH_FREQn_DRV_LS Configures the value of DRV_LS of the touch sensor for sampling frequency mode n. (R/W)

LP_ANA_TOUCH_FREQn_DRV_HS Configures the value of DRV_HS of the touch sensor for sampling frequency mode n. (R/W)

LP_ANA_TOUCH_FREQn_DBIAS Configures whether to enable the moisture tolerance function and configures the internal voltage of the touch sensor for sampling frequency mode n.
bit[0]: Configures whether to enable the moisture tolerance function for sampling frequency mode n.
0: Disable
1: Enable
bit[1-4]: Configures the internal voltage of the touch sensor for sampling frequency mode n. (R/W)
```