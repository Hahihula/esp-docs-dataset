

```markdown
Figure 6.3-2. ROM-Cache Structure

6.3.2.2 HP SRAM

This 384 KB HP SRAM is a read-and-write memory, accessed by the HP CPU and LP CPU through the instruction bus or data bus via their shared addresses 0x4080_0000 ~ 0x4085_FFFF, see Table 6.3-1.

6.3.2.3 LP SRAM

This 16 KB LP SRAM is a read-and-write memory, accessed by the HP CPU or LP CPU through the instruction bus or data bus via their shared addresses 0x5000_0000 ~ 0x5000_3FFF, see Table 6.3-1.

LP SRAM can be accessed by the following modes:

* high-speed mode, i.e., the LP SRAM is accessed in HP CPU clock frequency. In this case, HP CPU can access the LP SRAM without any latency. But the latency of LP CPU accessing LP SRAM ranges from a few dozen to dozens of LP CPU cycles.
* low-speed mode, i.e., the LP SRAM is accessed in LP CPU clock frequency. In this case, LP CPU can access the LP SRAM without any latency. But the latency of HP CPU accessing LP SRAM ranges from a few dozen to dozens of HP CPU cycles.

Switch the modes based on application scenarios.

* If the LP CPU is not working, switch to high-speed mode to improve the access speed of the HP CPU.
* If the LP CPU is executing code in the LP SRAM, switch to the low-speed mode.
* If the HP CPU is in sleep mode, it is a must to switch to the low-speed mode.

Mode Switch Configuration

* Configure LP_AON_FAST_MEM_MUX_SEL to select the mode needed:
    - 0: low-speed mode
    - 1: high-speed mode
* Set LP_AON_FAST_MEM_MUX_SEL_UPDATE to start mode switch.
* Read LP_AON_FAST_MEM_MUX_SEL_STATUS to check if mode switch is done:
    - 0: mode is switched
```