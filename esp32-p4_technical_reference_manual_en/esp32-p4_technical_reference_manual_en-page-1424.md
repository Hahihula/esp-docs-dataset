

```markdown
Chapter 24 Power Supply Detector (PSDET)

GoBack

Chapter 24

Power Supply Detector (PSDET)

24.1 Overview

The ESP32-P4 chip integrates a power supply detector, which is used to monitor the voltage of the on-chip HP system regulator. Specifically, this function is implemented by a voltage glitch detector, which prevents abnormal fluctuations and glitch attacks by real-time monitoring of the supply voltage. The power supply detector can operate continuously during the HP system operation.

24.2 Features

* Maintains monitoring during the chip's normal operation without requiring software intervention
* Automatically triggers a system reset when a voltage glitch of approximately 50 ns or longer is detected

24.3 Functional Description

The structure of the power supply detector based on voltage glitch detection is shown below:

![Figure 24.3-1. Structure of the ESP32-P4 Power Supply Detector](image)

VDD → Voltage Glitch Detector → RESET

Figure 24.3-1. Structure of the ESP32-P4 Power Supply Detector

The power supply detector of ESP32-P4 can continuously monitor the voltage of the power supply network while the chip is working. When an instantaneous voltage glitch—either too low or too high—lasts for more than 50 ns, it automatically triggers a system reset. The detection does not require register configuration. System resets triggered by this function will be recorded by the HP CPU reset cause register LP_CLKRST_HPCOREO_RESET_CAUSE, corresponding to the reset value 0x1B.

This function is disabled by default. To enable it, please flash the EFUSE_PVT_GLITCH_EN and EFUSE_PVT_GLITCH_MODE fields. For more information about eFuses, please refer to Chapter 8 eFuse Controller (EFUSE).

For information about reset, please refer to Chapter 10 Reset and Clock.
```