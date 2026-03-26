

```markdown
## 45.3 Architectural Overview

The figure below shows the architecture of the Analog I2C Controller.

![Figure 45.3-1. Analog I2C Controller Architecture](image_path)

*   Configuration Registers: A register module interfacing with the software, providing relevant configurations for the operation of the I2C master. This module controls the transmission address, data, etc., and monitors this transmission process by reading the status registers of I2CO/1_MST.
*   I2CO/1_MST: Two I2C masters that can independently configure analog modules in parallel. The I2C signals they generate will be selected by a subsequent MUX and output to the analog modules.
*   I2C signal MUX: A module that determines which analog master, I2CO_MST or I2C1_MST, configures a particular analog module.

## 45.4 Functional Description

### Transmission Rate Adjustment

The transmission rate and signal phase of the I2C signal can be configured by `ANA_I2C_MST_I2Cx_SDA_SIDE_GUARD` and `ANA_I2C_MST_I2Cx_SCL_PULSE_DUR`. The relationship between the register values and the waveform is shown in the following figure.
```