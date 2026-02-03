**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Subtitle:**
39.4.3 Functional Description

**Diagram Title:**
Figure 39.4-1. Temperature Sensor Overview

**Diagram Labels (from left to right, top to bottom):**
- ANALOG
- Tsensor
- XPD_SAR POWER_DOMAIN
- SENS_TSENS_OUT[7:0]
- SENS_TSENS READY
- SENS_TSENS_POWER_UPFORCE
- dump_out_fsm
- power_up_fsm

**Diagram Labels (right side, top to bottom):**
- RTC REG FILE
- ULP

**Text Content Below Diagrams and Descriptions:**

As shown in Figure 39.4-1, the temperature sensor can be started by software or by ULP coprocessor:

- **Started by software, i.e., by CPU or ULP-RISC-V configuring related registers:**
  - Set SENS_TSENS_POWER_UP FORCE and SENS_TSENS_POWER_UP to enable the temperature sensor.
  - Set SENSFORCE_XPD_SAR to force SAR ADC power on, and set SENS_TSENS_CLK_EN to enable temperature sensor clock.

- **Wait for a while, then configure SENS_TSENS_DUMP_OUT. The output value gradually approaches the actual temperature linearly as the measurement time increases.**

- Wait for SENS_TSENS_READY, and read the conversion result from SENS_TSENS_OUT.

- **Started by ULP-FSM:**
  - Clear SENS_TSENS_POWER_UP FORCE.
  - ULP-FSM has a built-in instruction for temperature sampling. Executing the instruction can easily complete temperature sampling, see Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V).

The actual temperature (°C) can be obtained by converting the output of temperature sensor via the following formula:

\[ (\text{°C}) = \frac{\text{(°C)}}{0.4386} * \text{VALUE} - 27.88 + \text{offset} - 20.52 \]

**Footer:**
Espressif Systems
1476 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback