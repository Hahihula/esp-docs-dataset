

```markdown
Register 30.2. HINF_CFG_DATA1_REG (0x0004)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)            |                                                                             |
| 31  |                        |                                                                             |
| 30  |                        |                                                                             |
| 29  | HINF_FUNC2_EPS        | The function 2 is not ready                                                 |
| 28  |                        |                                                                             |
| 27  | HINF_SDIO_VER         | Please refer to SDIO Specification for details. (R/W)                       |
| 26  |                        |                                                                             |
| 25  |                        |                                                                             |
| 24  |                        |                                                                             |
| 23  |                        |                                                                             |
| 22  | HINF_IOENABLE1        | The function 1 is ready                                                     |
| 21  | HINF_EMP             | Please refer to SDIO Specification for details. (R/W)                       |
| 20  | HINF_FUNC1_EPS       | O: Not support High-Speed mode                                              |
| 19  |                        |                                                                             |
| 18  | HINF_SDIO_IOREADY2   | The function 2 is ready                                                     |
| 17  | (reserved)           |                                                                             |
| 16  | HINF_SDIO_CD_ENABLE  | O: Disable                                                                  |
| 15  |                        |                                                                             |
| 14  | HINF_HIGH_SPEED_ENABLE | 1: Enable                                                                   |
| 13  |                        |                                                                             |
| 12  |                        |                                                                             |
| 11  |                        |                                                                             |
| 10  |                        |                                                                             |
| 9   |                        |                                                                             |
| 8   |                        |                                                                             |
| 7   |                        |                                                                             |
| 6   |                        |                                                                             |
| 5   |                        |                                                                             |
| 4   |                        |                                                                             |
| 3   |                        |                                                                             |
| 2   |                        |                                                                             |
| 1   |                        |                                                                             |
| 0   | Reset                 | 0x232                                                                        |

HINF_SDIO_IOREADY1 Configures the field IOR1 in SDIO CCCR and the field function 1 ready in SDIO CIS.
O: The function 1 is not ready
1: The function 1 is ready
Please refer to SDIO Specification for details.
(R/W)

HINF_HIGH_SPEED_ENABLE Configures whether to support SHS in SDIO CCCR.
O: Not support High-Speed mode
1: Support High-Speed mode
Please refer to SDIO Specification for details.
(R/W)

HINF_HIGH_SPEED_MODE Represents whether EHS status is enabled in SDIO CCCR.
O: Disabled
1: Enabled
Please refer to SDIO Specification for details.
(RO)

HINF_SDIO_CD_ENABLE Configures whether to enable SDIO card detection.
O: Disable
1: Enable
(R/W)

HINF_SDIO_IOREADY2 Configures the field IOR2 in SDIO CCCR and the field function 2 ready in SDIO CIS.
O: The function 2 is not ready
1: The function 2 is ready
Please refer to SDIO Specification for details.
(R/W)

HINF_IOENABLE2 Represents whether IOE2 is enabled in SDIO CCCR.
O: The function 2 is disabled
1: The function 2 is enabled
Please refer to SDIO Specification for details.
(RO)

Continued on the next page...
```