

```markdown
Chapter 40 MIPI CSI GoBack


The receiver enters high-speed mode following the low-power sequence of [LP-11 > LP-01 > LP-00]. Synchronization is achieved through a sync sequence of "00011101". After synchronization, the PHY receives high-speed data until a transition from LP-00 to LP-11 is detected on the lane.


40.5.2.6 Escape Mode

Escape mode allows asynchronous communication using data lanes at low speed. During Escape mode, the lane remains in low-power state. A data lane enters this mode after Escape mode request sequence [LP-11 > LP-10 > LP-00 > LP-01 > LP-00]. If an LP-11 state code is detected before the lane reaches LP-00, the request will be aborted, and the lane will return to stop state. Upon entering Escape mode, the transmitter sends an 8-bit command to indicate a requested action.

MIPI CSI only supports Ultra Low Power State (ULPS) in escape mode. The 8-bit command to enter ULPS is "b00011110". If the entry command is not valid, it will be ignored, and the receiver will wait until the transmitter returns to the stop state.

Ultra Low Power State

Ultra Low Power State involves the lowest power consumption, except for the Shut-Down state.

For data lanes, this mode is activated by sending an Ultra Low Power State entry command "00011110". After that, the clock lane and data lanes enter the space state (LP-00).

Figure 40.5-4 shows the ULPS sequences for clock and data lanes.
```