

```markdown
Chapter 52 Ethernet Media Access Control (EMAC)

Figure 52.4-5. RMII Interface

Note:
Figure 52.4-3 and Figure 52.4-5 uniformly use the signal name RX_DV to represent the receive-valid signal. In the MII interface, this corresponds to RX_DV, while in the RMII interface it corresponds to CRS_DV. The actual signal semantics depend on the selected Ethernet interface mode.

RMII Signals

The Reduced Media Independent Interface (RMII) specification reduces the number of pins between the microcontroller's Ethernet MAC and the external PHY at 10 Mbit/s or 100 Mbit/s. According to the IEEE 802.3u standard, an MII contains 16 pins for data and control. The RMII specification reduces the pin count to 7.

RMII has the following features:

* Supports an operating rate of 10 Mbit/s or 100 Mbit/s
* The clock reference must be 50 MHz.
* The same clock reference must be sourced externally both to the MAC and the external Ethernet PHY.
* Provides independent 2-bit wide TX and RX data paths.

RMII Clock

The 50 MHz RMII reference clock can be:

* Generated internally by ESP32-P4 and looped back via GPIOs. For GPIO configurations, please refer to Chapter 9 GPIO Matrix and IO MUX.
* Provided by the external crystal and obtained at GPIOs.

The RMII clock is shown in Figure 52.4-6.
```