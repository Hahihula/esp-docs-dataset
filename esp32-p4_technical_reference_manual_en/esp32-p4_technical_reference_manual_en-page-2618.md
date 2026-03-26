

```markdown
Figure 52.4-3. MII Interface
```

The MII interface signals are described below:

*   **MII_TX_CLK**: TX clock signal. This signal provides the reference timing for TX data transmission. It has two frequencies: 2.5 MHz at 10 Mbit/s, and 25 MHz at 100 Mbit/s.
*   **MII_TXD[3:0]**: A bundle of four transmit data signals driven by the MAC sublayer, and qualified (valid data) on the assertion of the MII_TX_EN signal. MII_TXD[0] is the lowest significant bit and MII_TXD[3] is the highest significant bit. When the MII_TX_EN signal is deasserted, the transmit data have no effect on the PHY.
*   **MII_TX_EN**: Transmission enable signal. This signal indicates that the MAC is presenting nibbles (4 bits) on the MII for transmission. It must be asserted synchronously (MII_TX_CLK) with the first nibble of the preamble and must remain asserted while all nibbles to be transmitted are presented to the MII.
*   **MII_TX_ERR**: Transmit error signal. The signal must be asserted for one or more clock periods (MII_TX_CLK) to indicate to the PHY layer that an error was detected somewhere in the frame.
*   **MII_RX_CLK**: RX clock signal. This signal provides the reference timing for RX data transmission. It has two frequencies: 2.5 MHz at 10 Mbit/s, and 25 MHz at 100 Mbit/s.
*   **MII_RXD[3:0]**: A bundle of four receive data signals driven by the MAC sublayer, and qualified (valid data) on the assertion of the MII_RX_DV signal. MII_RXD[0] is the lowest significant bit and MII_RXD[3] is the highest significant bit. When MII_RX_DV is deasserted and MII_RX_ERR is asserted, a specific MII_RXD[3:0] value is used to transfer specific information from the PHY.
*   **MII_RX_DV**: Receive data valid signal. This signal indicates that the PHY is presenting recovered and decoded nibbles on the MII for reception. It must be asserted synchronously (MII_RX_CLK) with the first recovered nibble of the frame and must remain asserted through the final recovered nibble. It must be deasserted prior to the first clock cycle that follows the final nibble. In order to receive the frame correctly, the MII_RX_DV signal must encompass the frame, starting no later than the SFD field.
```