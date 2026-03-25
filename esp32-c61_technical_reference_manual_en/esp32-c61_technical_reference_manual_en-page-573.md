

```markdown
Register 11.64. PMU_POWER_PD_LPPERI_CNTL_REG (0x010C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 30  | PMU_FORCE_LP_PERI_RESET        | Configures whether or not to force reset LPSYS_OFF domain.                 |
|     | 0: No effect                    | 1: Force reset                                                               |
|     | (R/W)                           |                                                                             |
| 29  | PMU_FORCE_LP_PERI_ISO          | Configures whether or not to enable the force isolation of LPSYS_OFF domain.|
|     | 0: No effect                    | 1: Enable                                                                    |
|     | (R/W)                           |                                                                             |
| 28  | PMU_FORCE_LP_PERI_PU           | Configures whether or not to force power up LPSYS_OFF domain.               |
|     | 0: No effect                    | 1: Force power up                                                            |
|     | (R/W)                           |                                                                             |
| 27  | PMU_FORCE_LP_PERI_NO_RESET     | Configures whether or not to forcefully prevent the reset of LP-SYS_OFF domain. This setting has a lower priority than PMU_FORCE_LP_PERI_RESET. |
|     | 0: No effect                    | 1: Force not reset                                                           |
|     | (R/W)                           |                                                                             |
| 26  | PMU_FORCE_LP_PERI_NO_ISO       | Configures whether or not to disable the force isolation of LP-SYS_OFF domain. This setting has a lower priority than PMU_FORCE_LP_PERI_ISO. |
|     | 0: No effect                    | 1: Disable                                                                  |
|     | (R/W)                           |                                                                             |
| 25  | PMU_FORCE_LP_PERI_PD           | Configures whether or not to force power down LPSYS_OFF domain.             |
|     | This setting has a lower priority than PMU_FORCE_LP_PERI_PU.                |                                                                             |
|     | 0: No effect                    | 1: Force power down                                                          |
|     | (R/W)                           |                                                                             |

Espressif Systems
573
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```