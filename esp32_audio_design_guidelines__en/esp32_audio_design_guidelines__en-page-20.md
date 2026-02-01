**Title:**
2. PCB Layout Design

**Figure Caption (Top):**
Figure 2-11. Reference Design for Ground Trace Routing

**Subtitle and Body Text:**

**2.3.3 Signal Traces Routing**

For the I2C, I2S, and UART groups, each respective group's traces should run parallel with as wide spacing as possible and be isolated from other groups with GND copper foil. If isolation is not possible due to limited space, please at least increase the interval between traces belonging to different groups.

- The signal traces for “Reset” should be as short as possible and isolated from other traces by ground traces or by extending the distance to reduce interference.
- The signal traces for audio input and output need to be enclosed with ground traces and surrounded by more ground holes for shielding.
- TouchPad trace routing must be done in accordance with the relevant guidelines to achieve the best performance.

The figures below show some relevant examples (the blue color represents ground copper).

**Figure Caption (Bottom):**
Figure 2-14. Reference Design UART Trace Routing

**Footer:**
Espressif
17/19
2019.01