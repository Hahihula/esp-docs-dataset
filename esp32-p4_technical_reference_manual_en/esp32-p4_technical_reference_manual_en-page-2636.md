

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack

Register 52.1. DMABUSMODE_REG (0x1000)

Continued from the previous page...

DMA_ARB_SCH Configures the arbitration scheme between the transmit and receive paths.
O: Weighted round-robin with RX:TX or TX:RX. In this case, the priority between the paths is according to the priority specified in PRI_RATIO.
1: Fixed priority (The transmit path has priority over receive path).
(R/W)

SW_RST Configures whether the MAC DMA Controller resets the logic and all internal registers of the MAC.
O: Release from reset
1: Reset
This bit is cleared automatically after the reset operation has completed in all of the ETH_MAC clock domains.
(R/WS/SC)
```

```markdown
Register 52.2. DMATXPOLLDEMAND_REG (0x1004)

TRANS_POLL_DEMAND Configures whether to enable the TX DMA to check if the DMA owns the current descriptor.
Any value: Enable

When this field is written, the DMA reads the current descriptor pointed to by DMATXCUR-RDESC_REG. If that descriptor is not available (owned by the Host), the transmission returns to the Suspend state and the Bit 2 (TU) of Register 5 (Status Register) is asserted. If the descriptor is available, the transmission resumes. (RO/WT)
```