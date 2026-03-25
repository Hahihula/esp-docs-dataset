

```markdown
Chapter 33 SPI Controller (SPI)

GoBack


Figure 33.7-1. SPI Clock Mode 0 or 2

End of Idle State ——— Begin Transfer End Begin of Idle State

SCK Edge Nr.    1   2   3   4   5   6   7   8   9   10  11  12  13  14  15  16
SCK (CPOL = 0)  ────────────────────────────────────────────────────────
SCK (CPOL = 1)  ────────────────────────────────────────────────────────

SAMPLE I MOSI/MISO   [Red/Black waveform pattern]
CHANGE O MOSI pin    ────────────────────────────────────────────────────────
CHANGE O MISO pin    ────────────────────────────────────────────────────────
SEL SS (O) Master only  ────────────────────────────────────────────────────────
SEL SS (I)

t_L = Minimum leading time before the first SCK edge
t_T = Minimum trailing time after the last SCK edge
t_I = Minimum idling time between transfers (minimum SS high time)
t_L, t_T, and t_I are guaranteed for the master mode and required for the slave mode.

MSB first (LSBFE = 0): MSB   Bit 6   Bit 5   Bit 4   Bit 3   Bit 2   Bit 1   LSB Minimum 1/2 SCK
LSB first (LSBFE = 1):    LSB   Bit 1   Bit 2   Bit 3   Bit 4   Bit 5   Bit 6   MSB      for t_I, t_L

Figure 33.7-2. SPI Clock Mode 1 or 3

End of Idle State ——— Begin Transfer End Begin of Idle State

SCK Edge Nr.    1   2   3   4   5   6   7   8   9   10  11  12  13  14  15  16
SCK (CPOL = 0)  ────────────────────────────────────────────────────────
SCK (CPOL = 1)  ────────────────────────────────────────────────────────

SAMPLE I MOSI/MISO   [Red/Black waveform pattern]
CHANGE O MOSI pin    ────────────────────────────────────────────────────────
CHANGE O MISO pin    ────────────────────────────────────────────────────────
SEL SS (O) Master only  ────────────────────────────────────────────────────────
SEL SS (I)

MSB first (LSBFE = 0): MSB   Bit 6   Bit 5   Bit 4   Bit 3   Bit 2   Bit 1   LSB Minimum 1/2 SCK
LSB first (LSBFE = 1):    LSB   Bit 1   Bit 2   Bit 3   Bit 4   Bit 5   Bit 6   MSB      for t_T, t_I

t_L = Minimum leading time before the first SCK edge, not required for back to back transfers
t_T = Minimum trailing time after the last SCK edge
t_I = Minimum idling time between transfers (minimum SS high time), not required for back to back transfers


1. Mode 0: CPOL = 0, CPHA = 0; SCK is 0 when the SPI is in idle state; data is changed on the falling edge of SCK and sampled on the rising edge. The first data is shifted out before the first falling edge of SCK.
2. Mode 1: CPOL = 0, CPHA = 1; SCK is 0 when the SPI is in idle state; data is changed on the rising edge of
```