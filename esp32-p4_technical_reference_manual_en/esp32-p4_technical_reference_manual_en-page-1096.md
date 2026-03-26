

```markdown
## 16.6 Registers

The addresses in this section are relative to Timer Group base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 16.1. TIMG_TxCONFIG_REG (x: 0-1) (0x0000+0x24*x)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | TIMG_Tx_EN                                                                   |
| 30  | TIMG_Tx_INCREASE                                                             |
| 29  | TIMG_Tx_AUTORELOAD                                                           |
| 28  | TIMG_Tx_DIVIDER                                                              |
| ... |                                                                             |
| 13  | (reserved)                                                                  |
| 12  | TIMG_Tx_DIVCNT_RST                                                          |
| 11  | TIMG_Tx_ALARM_EN                                                             |
| 10  | (reserved)                                                                  |
| 9   | 0                                                                            |
| ... |                                                                             |
| 0   | Reset                                                                       |

**TIMG_Tx_ALARM_EN** Configures whether to enable Timer Tx alarm function. This bit will be automatically cleared once an alarm occurs.
- O: Disable
- 1: Enable
(R/W/SC)

**TIMG_Tx_DIVCNT_RST** Configures to reset Timer Tx's clock divider counter.
- O: No effect
- 1: Reset
(WT)

**TIMG_Tx_DIVIDER** Represents Timer x clock (Tx_clk) prescaler value. (R/W)

**TIMG_Tx_AUTORELOAD** Configures to enable Timer Tx auto-reload function at the time of alarm.
- O: No effect
- 1: Enable
(R/W)

**TIMG_Tx_INCREASE** Configures the counting direction of Timer Tx time-base counter.
- O: Decrement
- 1: Increment
(R/W)

**TIMG_Tx_EN** Configures whether to enable Timer Tx time-base counter.
- O: Disable
- 1: Enable
(R/W/SS/SC)
```