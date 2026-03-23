

```markdown
Figure 27.7-1. SPI Clock Mode 0 or 2

End of Idle State — Begin Transfer End Begin of Idle State

SCK Edge Nr.
1   2   3   4   5   6   7   8   9   10  11  12  13  14  15  16

SCK (CPOL = 0) [Waveform]
SCK (CPOL = 1) [Waveform]

SAMPLE I MOSI/MISO [Vertical ticks at positions: approx. 3,7,11,15]

CHANGE O MOSI pin [Square wave pattern]
CHANGE O MISO pin [Square wave pattern]

SEL SS (O) Master only
SEL SS (I)

t_L   t_T   t_I   t_L

MSB first (LSBFE = 0): MSB Bit 6 Bit 5 Bit 4 Bit 3 Bit 2 Bit 1 LSB Minimum 1/2 SCK
LSB first (LSBFE = 1): LSB Bit 1 Bit 2 Bit 3 Bit 4 Bit 5 Bit 6 MSB for t_T, t_I, t_L

t_L = Minimum leading time before the first SCK edge
t_T = Minimum trailing time after the last SCK edge
t_I = Minimum idling time between transfers (minimum SS high time)

t_L, t_T and t_I are guaranteed for the master mode and required for the slave mode.

Figure 27.7-2. SPI Clock Mode 1 or 3

End of Idle State — Begin Transfer End Begin of Idle State

SCK Edge Nr.
1   2   3   4   5   6   7   8   9   10  11  12  13  14  15  16

SCK (CPOL = 0) [Waveform]
SCK (CPOL = 1) [Waveform]

SAMPLE I MOSI/MISO [Vertical ticks at positions: approx. 3,7,11,15]

CHANGE O MOSI pin [Square wave pattern]
CHANGE O MISO pin [Square wave pattern]

SEL SS (O) Master only
SEL SS (I)

t_L   t_T   t_I   t_L

MSB first (LSBFE = 0): MSB Bit 6 Bit 5 Bit 4 Bit 3 Bit 2 Bit 1 LSB Minimum 1/2 SCK
LSB first (LSBFE = 1): LSB Bit 1 Bit 2 Bit 3 Bit 4 Bit 5 Bit 6 MSB for t_T, t_I, t_L

t_L = Minimum leading time before the first SCK edge, not required for back to back transfers
t_T = Minimum trailing time after the last SCK edge
t_I = Minimum idling time between transfers (minimum SS high time), not required for back to back transfers

1. Mode 0: CPOL = 0, CPHA = 0; SCK is 0 when the SPI is in idle state; data is changed on the negative edge of SCK and sampled on the positive edge. The first data is shifted out before the first negative edge of SCK.
```