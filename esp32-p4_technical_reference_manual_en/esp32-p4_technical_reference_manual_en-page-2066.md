

```markdown
| Frequency Range (Mbps) | hsfreqrange[5:0] |
|-------------------------|------------------|
| 1450-1500               | 111100           |

When `CSI_HOST_DPHY_RSTZ` and `CSI_HOST_PHY_SHUTDOWNZ` are set to 1, the MIPI RX D-PHY leaves the Shut-Down state and starts the initialization procedure.

### 40.5.2.3 AFE Initialization

After releasing `CSI_HOST_DPHY_RSTZ` and `CSI_HOST_PHY_SHUTDOWNZ`, the PHY begins an initialization sequence for normal operation. It is recommended to release `CSI_HOST_PHY_SHUTDOWNZ` before `CSI_HOST_DPHY_RSTZ`. Additionally, ensure that `CSI_DPHY_CFG_CLK` (refer to Table 10.2-5 in Chapter 10 *Reset and Clock* for details) is available and stable at this point.

The initialization sequence includes several steps, such as enabling internal blocks and performing internal calibrations. Once completed, control transfers to the lanes, which manage power for LP/HS requests from the transmitter by enabling or disabling the corresponding receivers.

Set `CSI_HOST_PHY_STOPSTATEDATA_n` and `CSI_HOST_PHY_STOPSTATECLK` to 1 to perform all initialization steps. In this state, both clock and data lanes are in stop state (LP-11).

The initialization period (TINIT) is a protocol-dependent parameter with a minimum duration of 100 µs, as defined by the specification. After setting `CSI_HOST_PHY_STOPSTATEDATA_n` and `CSI_HOST_PHY_STOPSTATECLK` to 1, the software should wait more than 100 µs before starting camera data reception.

### 40.5.2.4 Control Mode

After completing AFE initialization, the MIPI RX D-PHY remains in Control mode by default. It receives the LP-11 state code (stop state) on the lines until a request is made. Upon receiving a request, the PHY enters either High-Speed Data Reception mode, Escape mode, or Ultra Low Power State. All requests must begin and end with the lanes in the stop state.

### 40.5.2.5 High-Speed Data Reception Mode

In High-Speed Data Reception mode, the PHY receives data in bursts. The lane operates in high-speed mode only during these bursts.

As shown in Figure 40.5-3, a burst consists of three parts: the low-power initialization sequence, the high-speed data payload, and the end of reception sequence.
```