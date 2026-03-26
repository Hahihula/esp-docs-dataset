

```markdown
• MII_CRS: Carrier sense signal. When the transmit or receive medium is non-idle, the signal is asserted by the PHY. When the transmit or receive medium is idle, the signal is deasserted by the PHY. The PHY must ensure that the MII_CRS signal remains asserted throughout the duration of a collision condition. This signal does not need to be synchronized with the TX and RX clocks. In full duplex mode the state of this signal is don't care for the MAC sublayer.
• MII_COL: Collision detection signal. This signal must be asserted by the PHY upon detection of a collision on the medium and must remain asserted while the collision condition persists. This signal is not required to transition synchronously with respect to the TX and RX clocks. In full duplex mode, the state of this signal is don't care for the MAC sublayer.
• MII_RX_ERR: Receive error signal. The signal must be asserted for one or more clock periods (MII_RX_CLK) to indicate to the MAC sublayer that an error was detected somewhere in the frame.
• MDIO and MDC: Management data input/output and management data clock signal. The two signals constitute a serial bus defined for the Ethernet family of IEEE 802.3 standards, used to transfer control and data information to the PHY, see section Station Management Agent (SMA) Interface.

MII Clock

In MII mode, there are clock signals in two directions between MII and the PHY, namely clk_tx and clk_rx. clk_tx is used to synchronize the TX data, and clk_rx is used to synchronize the RX data. Both clocks are provided by the PHY.

Figure 52.4-4. MII Clock

52.4.4.2 Reduced Media Independent Interface: RMII

RMII interface signals are shown in Figure 52.4-5.
```