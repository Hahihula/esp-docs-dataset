

```markdown
Register 19.4. HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG (0x0080)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31-7      | (reserved)                                                                  |
| 6         | HP_SYSTEM_BITSCRAMBLER_TX_SEL                                               |
| 5-0       | HP_SYSTEM_BITSCRAMBLER_RX_SEL                                               |

HP_SYSTEM_BITSCRAMBLER_RX_SEL Configures to select the DMA-capable peripheral for BitScrambler's RX channel.

1: GPSPI2
2: UHCI0
3: I2SO
4: AES
5: SHA
6: ADC
7: PARL_IO
others: NONE
(R/W)

HP_SYSTEM_BITSCRAMBLER_TX_SEL Configures to select the DMA-capable peripheral for BitScrambler's TX channel.

1: GPSPI2
2: UHCI0
3: I2SO
4: AES
5: SHA
6: ADC
7: PARL_IO
others: Reserved
(R/W)
```