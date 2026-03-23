

```markdown
Register 34.2. HINF_CFG_DATA1_REG (0x0004)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 25  |                             | (reserved)                                                                  |
| 24  | HINF_FUNC2_EPS              |                                                                             |
| 23  |                             | (reserved)                                                                  |
| 12  | HINF_SDIO_VER               |                                                                             |
| 11  |                             | (reserved)                                                                  |
| 10  | HINF_IOENABLE1              |                                                                             |
| 9   | HINF_EMPCODE_DISABLE       |                                                                             |
| 8   | HINF_FUNC_CD_ENABLE         |                                                                             |
| 7   | HINF_SDIO_IOREADY2          | Configures the field IOR2 in SDIO CCCR and the field function 2 ready in SDIO CIS. O: The function 2 is not ready<br>1: The function 2 is ready<br>Please refer to SDIO Specification for details.<br>(R/W) |
| 6   |                             | (reserved)                                                                  |
| 5   | HINF_SDIO_CD_ENABLE         | Configures whether to enable SDIO card detection.<br>O: Disable<br>1: Enable<br>(R/W) |
| 4   | HINF_HIGH_SPEED_ENABLE      | Configures whether to support SHS in SDIO CCCR.<br>O: Not support High-Speed mode<br>1: Support High-Speed mode<br>Please refer to SDIO Specification for details.<br>(R/W) |
| 3   |                             | (reserved)                                                                  |
| 2   | HINF_HIGH_SPEED_MODE        | Represents whether EHS status is enabled in SDIO CCCR.<br>O: Disabled<br>1: Enabled<br>Please refer to SDIO Specification for details.<br>(RO) |
| 1   |                             | (reserved)                                                                  |
| 0   | Reset                       |                                                                             |

HINF_SDIO_IOREADY1 Configures the field IOR1 in SDIO CCCR and the field function 1 ready in SDIO CIS.
O: The function 1 is not ready
1: The function 1 is ready
Please refer to SDIO Specification for details.
(R/W)

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