

```markdown
Register 39.2. HINF_CFG_DATA1_REG (0x0004)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 25  |                                 | (reserved)                                                                  |
| 24  | HINF_FUNC2_EPS                  |                                                                             |
| 23  |                                 |                                                                             |
| 12  | HINF_SDIO_VER                   |                                                                             |
| 11  | HINF_IOENABLE1                  |                                                                             |
| 10  | HINF_EMPI                      |                                                                             |
| 9   | HINF_FUNC_CD_DISABLE           |                                                                             |
| 8   | HINF_IOENABLE2                 |                                                                             |
| 7   | (reserved)                    |                                                                             |
| 6   | HINF_SDIO_IOREADY2             |                                                                             |
| 5   | HINF_HIGH_SPEED_ENABLE         |                                                                             |
| 4   | HINF_HIGH_SPEED_MODE           |                                                                             |
| 3   | HINF_SDIO_CD_ENABLE            |                                                                             |
| 2   |                                 | (reserved)                                                                  |
| 1   |                                 |                                                                             |
| 0   | O                              | Reset                                                                       |

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
```
Continued on the next page...
```