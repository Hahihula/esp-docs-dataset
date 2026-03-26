
```markdown
Register 52.27. EMACINTS_REG (0x0038)

LPIINTS    The raw interrupt status of EMAC_LPI_INT. (RO)
TINTS      The raw interrupt status of TS_TRI_INT. (R/SS/RC)
PMTINTS    The raw interrupt status of EMAC_PMP_INT. (RO)


Register 52.28. EMACINTMASK_REG (0x003C)

LPIINTMASK Write 1 to mask EMAC_LPI_INT.(R/W)
TSINTMASK   Write 1 to mask TS_TRI_INT. (R/W)
PMTINTMASK  Write 1 to mask EMAC_PMP_INT. (R/W)


Register 52.29. EMACADDROHIGH_REG (0x0040)

ADDRESS_ENABLEO This bit is always set to 1. (RO)
MAC_ADDRESO_HI Configures the upper 16 bits of the first 6-byte MAC address [47:32].
The MAC uses this field for filtering the received frames and inserting the MAC address in the
Transmit Flow Control (PAUSE) Frames. (R/W)
```