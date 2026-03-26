

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.58. HP_SYSTEM_GMAC_CTRL0_REG (0x014C)
```

```text
(reserved)
31 7 6 5 4 2 1 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

HP_SYSTEM_SYS_PTP_PPS Represents pulse per second output from Ethernet MAC. (RO)

HP_SYSTEM_SYS_SBD_FLOWCTRL Configures sideband flow control signal.
O: No effect
1: Instruct Ethernet MAC to transmit Pause frames in Full-duplex mode and enable back-pressure in half-duplex mode.
(R/W)

HP_SYSTEM_SYS_PHY_INTF_SEL Configures Ethernet PHY interface.
O: MII
4: RMII
Others: Reserved
(R/W)

HP_SYSTEM_SYS_GMAC_MEM_CLK_FORCE_ON Configures whether or not to force enable the memory clock of GMAC memory.
O: No effect
1: Force on
(R/W)

HP_SYSTEM_SYS_GMAC_RST_CLK_TX_N Represents an active-low reset signal synchronized to the Ethernet MAC Tx clock. (RO)

HP_SYSTEM_SYS_GMAC_RST_CLK_RX_N Represents an active-low reset signal synchronized to the Ethernet MAC Rx clock. (RO)
```