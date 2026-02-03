**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Header:**
Register 39.19, SENS_SAR_TSENS_CTRL_REG (0x050)

**Table Description:**
- The table lists various control register bits for the temperature sensor.
- Bits are labeled from "reserved" to specific functions like "SENS_TSENS_OUT", "SENS_TSENS READY", etc.

**Bit Labels and Functions:**
- 31, reserved
- 25–24, SENS_TSENS_INInv (0)
- 23–22, SENS_TSENS_CLK_DIV (0)
- 21, SENS_TSENS_POWER_UP FORCE (0)
- 6, SENS_TSENS_OUT (0)
- 14–13, reserved
- 12–9, SENS_TSENS_INInv (0)
- 8, SENS_TSENS READY (0)
- 7, reserved

**Bit Values:**
- The binary values for each bit are shown as "0" or "1".

**Descriptions of Register Bits:**
- **SENS_TSENS_OUT:** Temperature sensor data out. (RO) - Read Only
- **SENS_TSENS_READY:** Indicate temperature sensor ready. (RO) - Read Only
- **SENS_TSENS_INT_EN:** Enable temperature sensor to send out interrupt. (R/W) - Read/Write
- **SENS_TSENS_INInv:** Invert temperature sensor data. (R/W) - Read/Write
- **SENS_TSENS_CLK_DIV:** Temperature sensor clock divider. (R/W) - Read/Write
- **SENS_TSENS_POWER_UP:** Temperature sensor power up. (R/W) - Read/Write
- **SENS_TSENS_POWER_UP FORCE:** 1: data dump out and power up controlled by software. 0: by FSM. (R/W) - Read/Write

**Additional Information:**
- SENS_TSENS_DUMP_OUT is active when SNES_TSENS_POWER_UP FORCE = 1.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback