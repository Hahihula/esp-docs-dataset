

```markdown
Register 15.2. TIMG_TOLO_REG (0x0004)

TIMG_TO_LO Represents the low 32 bits of the time-base counter of timer O. Valid only after writing to TIMG_TOUPDATE_REG.
Measurement unit: TO_clk
(RO)

Register 15.3. TIMG_TOHI_REG (0x0008)

TIMG_TO_HI Represents the high 22 bits of the time-base counter of timer O. Valid only after writing to TIMG_TOUPDATE_REG.
Measurement unit: TO_clk
(RO)

Register 15.4. TIMG_TOUPDATE_REG (0x000C)

TIMG_TO_UPDATE Configures to latch the counter value.
0: Latch
1: Latch

Note that writing either 0 or 1 to this bit will trigger latching of the counter value.
(R/W/SC)
```