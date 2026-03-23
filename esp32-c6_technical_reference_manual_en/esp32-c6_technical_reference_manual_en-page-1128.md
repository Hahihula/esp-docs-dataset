

```markdown
Register 34.2. HINF_CFG_DATA1_REG (0x0004)
```

Continued from the previous page...

HINF_CD_DISABLE Represents whether CD is disabled in SDIO CCCR.
- 0: Enabled
- 1: Disabled
Please refer to SDIO Specification for details.
(RO)

HINF_FUNC1_EPS Represents function 1 EPS status in SDIO FBR.
- 0: The function 1 operates in Higher Current Mode
- 1: The function 1 works in Lower Current Mode
Please refer to SDIO Specification for details.
(RO)

HINF_EMP Represents EMPC status in SDIO CCCR.
- 0: Master Power Control is disabled
- 1: Master Power Control is enabled
Please refer to SDIO Specification for details.
(RO)

HINF_IOENABLE1 Represents IOE1 status in SDIO CCCR.
- 0: The function 1 is disabled
- 1: The function 1 is enabled
Please refer to SDIO Specification for details.
(RO)

HINF_SDIO_VER Configures SD bit[3:0], SDIO bit[3:0], CCCR bit[3:0] in SDIO CCCR.
- HINF_SDIO_VER[11:8] mapping to SD bit[3:0]
- HINF_SDIO_VER[7:4] mapping to SDIO bit[3:0]
- HINF_SDIO_VER[3:0] mapping to CCCR bit[3:0]
Please refer to SDIO Specification for details.
(R/W)

HINF_FUNC2_EPS Represents function 2 EPS status in SDIO FBR.
- 0: The function 2 operates in Higher Current Mode
- 1: The function 2 works in Lower Current Mode
Please refer to SDIO Specification for details.
(RO)
```