

```markdown
Register 52.25. EMACLPI_CSR_REG (0x0030)
```

Continued from the previous page...

**RLPIEN** Represents the receive LPI entry state.
- O: Inactive
- 1: The EMAC Receiver has received an LPI pattern and entered the LPI state (R/SS/RC)

**TLPIEX** Represents the transmit LPI exit state.
- O: Inactive
- 1: The EMAC transmitter has exited the LPI state after the user has cleared the LPIEN bit and the LPI_TW_TIMER has expired (R/SS/RC)

**TLPIEN** Represents the transmit LPI entry state.
- O: Inactive
- 1: The EMAC Transmitter has entered the LPI state because of the setting of the LPIEN bit (R/SS/RC)

Register 52.26. EMACLPLITIMERSCONTROL_REG (0x0034)
```
┌───────────────────────────────────────────────────────────────────────────────┐
│ 31 │ 26 │ 25 │ 16 │ 15 │ ... │ 0 │
├────┼────┼────┼────┼────┼────┼────┤
│ 0 │ 0 │ 0 │ 0 │ x │ 3 │ E │ 8 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ Reset │
└───────────────────────────────────────────────────────────────────────────────┘
```
- (reserved)
- LPI_LS_TIMER
- LPI_TW_TIMER

**LPI_LS_TIMER** Configures the minimum time for which the link status from the PHY should be up.  
Measurement unit: millisecond.  
The default value is 1000 (1 second) as defined in the IEEE standard.  
(R/W)

**LPI_TW_TIMER** Configures the minimum time for which the MAC waits after it stops transmitting the LPI pattern to the PHY and before it resumes the normal transmission.  
Measurement unit: millisecond.  
The TLPIEX status bit is set after the expiry of this timer.  
(R/W)
```