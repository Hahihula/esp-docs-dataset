

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.50. HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG (0x0140)
```

```text
(reserved)
```

| Bit | Description |
|-----|-------------|
| 31  |             |
| 30  |             |
| 29  |             |
| 28  |             |
| 27  |             |
| 26  |             |
| 25  |             |
| 24  |             |
| 23  |             |
| 22  |             |
| 21  |             |
| 20  |             |
| 19  |             |
| 18  |             |
| 17  |             |
| 16  |             |
| 15  |             |
| 14  |             |
| 13  |             |
| 12  |             |
| 11  |             |
| 10  |             |
| 9   |             |
| 8   |             |
| 7   |             |
| 6   |             |
| 5   |             |
| 4   |             |
| 3   |             |
| 2   |             |
| 1   |             |
| 0   | Reset        |

```markdown
HP_SYSTEM_BITSCRAMBLER_PERI_RX_SEL Configures to select the DMA-capable peripheral for BitScrambler's Rx channel.

0: LCD_CAM
1: GPSPI2
2: GPSPI3
3: PARL_IO
4: AES
5: SHA
6: ADC
7: I2SO
8: I2S1
9: I2S2
10: I3C_MST
11: UHCIO
12: RMT
others: NONE
(R/W)
```

```markdown
HP_SYSTEM_BITSCRAMBLER_PERI_TX_SEL Configures to select the DMA-capable peripheral for BitScrambler's Tx channel.

0: LCD_CAM
1: GPSPI2
2: GPSPI3
3: PARL_IO
4: AES
5: SHA
6: ADC
7: I2SO
8: I2S1
9: I2S2
10: I3C_MST
11: UHCIO
12: RMT
others: NONE
(R/W)
```

```markdown
Espressif Systems    1285

Submit Documentation Feedback      ESP32-P4 TRM PRELIMINARY
```