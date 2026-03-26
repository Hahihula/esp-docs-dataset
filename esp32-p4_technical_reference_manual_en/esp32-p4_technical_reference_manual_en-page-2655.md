

```markdown
Continued from the previous page...

FCBBA Configures whether to enable a Pause Control frame in the full-duplex mode, and whether to activate the back-pressure function in the half-duplex mode if the TFCE bit is set.

0: Disable
1: Enable

In the full-duplex mode, this bit should be read as 0 before writing to the Flow Control register. To initiate a Pause control frame, the Application must set this bit to 1. During a transfer of the Control Frame, this bit continues to be set to signify that a frame transmission is in progress. After the completion of Pause control frame transmission, the MAC resets this bit to 0. The Flow Control register should not be written to until this bit is cleared. (R/W/S/SC)

In the half-duplex mode, when this bit is set (and TFCE is set), then backpressure is asserted by the MAC. During backpressure, when the MAC receives a new frame, the transmitter starts sending a JAM pattern resulting in a collision. When the MAC is configured for the full-duplex mode, the BPA is automatically disabled. (R/W)
```