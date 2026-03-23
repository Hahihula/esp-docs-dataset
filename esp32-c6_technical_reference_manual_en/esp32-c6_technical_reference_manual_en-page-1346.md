

```markdown
Register 38.1. PARL_IO_RX_CFGO_REG (0x0000)

| Bit | 31 | 30 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 19 | 18 | 17 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|
|     |    |    |    |    |    |    | Oxo| O  | O  | O  | O  | O  |   |   | Reset |
| Value | 0  | 0  | 0  | 0  | 0  | OxO| 0  | 0  | 0  | 0  | 0  | 0x00 | 0 | 0 |    |

PARL_IO_RX_EOF_GEN_SEL Configures the generating mechanism of GDMA SUC EOF.
- 0: Generate GDMA SUC EOF by the configured data byte length
- 1: Generate GDMA SUC EOF by the external enable signal (R/W)

PARL_IO_RX_START Configures whether to start RX global data sampling.
- 0: No effect
- 1: Start (R/W)

PARL_IO_RX_DATA_BYTELEN Configures data byte length received by RX. (R/W)

PARL_IO_RX_SW_EN Configures whether to enable software data sampling.
- 0: Disable
- 1: Enable (R/W)

PARL_IO_RX_PULSE_SUBMODE_SEL Configures Pulse Enable sub-mode.
- 0: Positive pulse start (data bit included) & Positive pulse end (data bit included)
- 1: Positive pulse start (data bit included) & Positive pulse end (data bit excluded)
- 2: Positive pulse start (data bit excluded) & Positive pulse end (data bit included)
- 3: Positive pulse start (data bit excluded) & Positive pulse end (data bit excluded)
- 4: Positive pulse start (data bit included) & Length end
- 5: Positive pulse start (data bit excluded) & Length end
- 6: Negative pulse start (data bit included) & Negative pulse end(data bit included)
- 7: Negative pulse start (data bit included) & Negative pulse end (data bit excluded)
- 8: Negative pulse start (data bit excluded) & Negative pulse end (data bit included)
- 9: Negative pulse start (data bit excluded) & Negative pulse end (data bit excluded)
- 10: Negative pulse start (data bit included) & Length end
- 11: Negative pulse start (data bit excluded) & Length end (R/W)

Continued on the next page...
```