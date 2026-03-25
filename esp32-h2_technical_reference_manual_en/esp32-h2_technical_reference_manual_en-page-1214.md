

```markdown
## 38.10 Registers

The addresses in this section are relative to Parallel IO Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 38.1. PARL_IO_RX_MODE_CFG_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 30   | 29   | 27   | 26   | 25   | 24   | 21   | 20   | ... | 0    |
| 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x7 |      | Reset|

**PARL_IO_RX_EXT_EN_SEL** Configures the RX external enable signal from IO PAD. (R/W)

**PARL_IO_RX_SW_EN** Configures whether to enable data sampling by software.
- 0: Disable
- 1: Enable
(R/W)

**PARL_IO_RX_EXT_EN_INV** Configures whether to invert the external enable signal.
- 0: No effect
- 1: Invert
(R/W)

**PARL_IO_RX_PULSE_SUBMODE_SEL** Configures the RXD pulse sampling sub-mode.
- 0: Positive pulse start (data bit included) & Positive pulse end (data bit included)
- 1: Positive pulse start (data bit included) & Positive pulse end (data bit excluded)
- 2: Positive pulse start (data bit excluded) & Positive pulse end (data bit included)
- 3: Positive pulse start (data bit excluded) & Positive pulse end (data bit excluded)
- 4: Positive pulse start (data bit included) & Length end
- 5: Positive pulse start (data bit excluded) & Length end
(R/W)

**PARL_IO_RX_SMP_MODE_SEL** Configures the RXD sampling mode.
- 0: External Level Enable mode
- 1: External Pulse Enable mode
- 2: Internal Software Enable mode
(R/W)
```