

```markdown
Register 16.2. TIMG_TxLO_REG (x: 0-1) (0x0004+0x24*x)

TIMG_Tx_LO Represents the low 32 bits of the time-base counter of Timer Tx. Valid only after writing to TIMG_TxUPDATE_REG.
Measurement unit: Tx_clk.
(RO)

Register 16.3. TIMG_TxHI_REG (x: 0-1) (0x0008+0x24*x)

TIMG_Tx_HI Represents the high 22 bits of the time-base counter of Timer Tx. Valid only after writing to TIMG_TxUPDATE_REG.
Measurement unit: Tx_clk.
(RO)

Register 16.4. TIMG_TxUPDATE_REG (x: 0-1) (0x000C+0x24*x)

TIMG_Tx_UPDATE Configures to latch the counter value.
0: Latch
1: Latch
(R/W/SC)
```