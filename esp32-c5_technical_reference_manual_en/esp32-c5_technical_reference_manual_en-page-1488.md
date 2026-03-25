

```markdown
Register 39.40. SLCHOST_CONF_REG (0x01F0)

| 31 | 28 | 27 | 26 | 20 | 19 | 15 | 14 | 10 | 9 | 5 | 4 | 0 |
|-----|----|----|----|----|----|----|----|----|---|---|---|---|
| OxO | 0  | 0x0|     | OxO|    |    |    |    |   | OxO| OxO| Reset |

SLCHOST_FRC_SDIO11 Configure 1 to bit[4] to force drive CMD signal at the falling clock edge. Configures 1 to bit[3:0] corresponding bit to force drive DAT[3:0] signal corresponding bit at the falling clock edge. (R/W)

SLCHOST_FRC_SDIO20 Configure 1 to bit[4] to force drive CMD signal at the rising clock edge. Configures 1 to bit[3:0] corresponding bit to force drive DAT[3:0] signal corresponding bit at the rising clock edge. (R/W)

SLCHOST_FRC_NEG_SAMP Configure 1 to bit[4] to force sample CMD signal at the falling clock edge. Configures 1 to bit[3:0] corresponding bit to force sample DAT[3:0] signal corresponding bit at the falling clock edge. (R/W)

SLCHOST_FRC_POS_SAMP Configure 1 to bit[4] to force sample CMD signal at the rising clock edge. Configures 1 to bit[3:0] corresponding bit to force sample DAT[3:0] signal corresponding bit at the rising clock edge. (R/W)

SLCHOST_HSPEED_CON_EN Configures 1 to this bit, configures 1 to HINF_HIGHSPEED_ENABLE, and then the host configures 1 to EHS in CCCR to force drive CMD and DAT signals at the rising clock edge. (R/W)
```