
```markdown
Register 5.17. DMAC_CHn_AXI_IDO_REG (0x0150)

DMAC_CHn_AXI_READ_ID_SUFFIX   Configure the least significant bit of AXI read ID. (R/W)
DMAC_CHn_AXI_WRITE_ID_SUFFIX  Configure the least significant bit of AXI write ID. (R/W)


Register 5.18. DMAC_INTSTATUSO_REG (0x0030)

DMAC_CHn_INTSTAT (n: 1-4) Indicates the interrupt status for channel n.
    1: Interrupt is active
    0: Interrupt is inactive
    (RO)

DMAC_COMMONREG_INTSTAT Indicates the common register interrupt status.
    1: Interrupt is active
    0: Interrupt is inactive
    (RO)
```