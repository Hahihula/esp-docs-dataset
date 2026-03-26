

```markdown
Register 16.5. TIMG_TxALARMLO_REG (x: 0-1) (0x0010+0x24*x)

TIMG_Tx_ALARM_LO Configures the low 32 bits of Timer Tx alarm trigger time-base counter value.
Valid only when TIMG_Tx_ALARM_EN is 1.
Measurement unit: Tx_clk.
(R/W)
```

```markdown
Register 16.6. TIMG_TxALARMHI_REG (x: 0-1) (0x0014+0x24*x)

TIMG_Tx_ALARM_HI Configures the high 22 bits of Timer Tx alarm trigger time-base counter value.
Valid only when TIMG_Tx_ALARM_EN is 1.
Measurement unit: Tx_clk.
(R/W)
```

```markdown
Register 16.7. TIMG_TxLOADLO_REG (x: 0-1) (0x0018+0x24*x)

TIMG_Tx_LOAD_LO Configures low 32 bits of the value that a reload will load onto Timer Tx time-base counter.
Measurement unit: Tx_clk.
(R/W)
```