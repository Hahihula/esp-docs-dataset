

```markdown
Chapter 58 Parallel IO Controller (PARLIO)

Register 58.3. PARL_IO_RX_GENRL_CFG_REG (0x0008)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 30  | PARL_IO_RX_EOF_GEN_SEL |
| 29  | PARL_IO_RX_TIMEOUT_EN |
|     |                     |
| 28  | PARL_IO_RX_GATING_EN |
|     |                     |
| 13-12 | (reserved)        |
| 11  | O                   |
| ... | O                   |
| 0   | Reset               |

PARL_IO_RX_GATING_EN Configures whether to enable the clock gating of the RX output clock.
O: Disable
1: Enable
(R/W)

PARL_IO_RX_TIMEOUT_THRES Configures the threshold of the RX timeout counter. (R/W)

PARL_IO_RX_TIMEOUT_EN Configures whether to enable the timeout function to generate GDMA ERR EOF.
O: Disable
1: Enable
(R/W)

PARL_IO_RX_EOF_GEN_SEL Configures the generation mechanism of GDMA SUC EOF.
O: Generate GDMA SUC EOF by the configured data bit length
1: Generate GDMA SUC EOF by the external enable signal
(R/W)

Register 58.4. PARL_IO_RX_START_CFG_REG (0x000C)

| Bit | Description          |
|-----|----------------------|
| 31  | (reserved)           |
| 30  | PARL_IO_RX_START     |
| ... | O                    |
| 0   | Reset                |

PARL_IO_RX_START Configures whether to start RX data sampling.
O: No effect
1: Start
(R/W)
```