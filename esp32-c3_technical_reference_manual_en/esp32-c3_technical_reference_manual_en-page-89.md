

```markdown
Register 2.30. GDMA_OUT_PRI_CHn_REG (n: 0-2) (0x0FC+192*n)

GDMA_TX_PRI_CHn The priority of TX channel O. The larger the value, the higher the priority. (R/W)


Register 2.31. GDMA_IN_PERI_SEL_CHn_REG (n: 0-2) (0x00A0+192*n)

GDMA_PERI_IN_SEL_CHn This register is used to select peripheral for RX channel O. 0: SPI2. 1: reserved. 2: UHCI0. 3: I2S. 4: reserved. 5: reserved. 6: AES. 7: SHA. 8: ADC; 9 ~ 63: Invalid. (R/W)


Register 2.32. GDMA_OUT_PERI_SEL_CHn_REG (n: 0-2) (0x0100+192*n)

GDMA_PERI_OUT_SEL_CHn This register is used to select peripheral for TX channel O. 0: SPI2. 1: reserved. 2: UHCI0. 3: I2S. 4: reserved. 5: reserved. 6: AES. 7: SHA. 8: ADC; 9 ~ 63: Invalid. (R/W)
```