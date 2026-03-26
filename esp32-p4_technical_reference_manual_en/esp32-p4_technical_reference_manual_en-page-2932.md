

```markdown
## 58.10 Registers

The addresses in this section are relative to Parallel IO Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 58.1. PARL_IO_RX_MODE_CFG_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 30  | O: Disable<br>1: Enable<br>(R/W) |
| 29  | PARL_IO_RX_EXT_EN_SEL Configures the RX external enable signal from IO PAD. (R/W) |
| 28  | PARL_IO_RX_SW_EN Configures whether to enable data sampling by software.<br>O: Disable<br>1: Enable<br>(R/W) |
| 27  | PARL_IO_RX_EXT_EN_INV Configures whether to invert the external enable signal.<br>O: No effect<br>1: Invert<br>(R/W) |
| 26  | PARL_IO_RX_PULSE_SUBMODE_SEL Configures the RXD pulse sampling sub-mode.<br>0: Positive pulse start (data bit included) &amp; Positive pulse end (data bit included)<br>1: Positive pulse start (data bit included) &amp; Positive pulse end (data bit excluded)<br>2: Positive pulse start (data bit excluded) &amp; Positive pulse end (data bit included)<br>3: Positive pulse start (data bit excluded) &amp; Positive pulse end (data bit excluded)<br>4: Positive pulse start (data bit included) &amp; Length end<br>5: Positive pulse start (data bit excluded) &amp; Length end<br>(R/W) |
| 25  | PARL_IO_RX_SMP_MODE_SEL Configures the RXD sampling mode.<br>0: External Level Enable mode<br>1: External Pulse Enable mode<br>2: Internal Software Enable mode<br>(R/W) |
```