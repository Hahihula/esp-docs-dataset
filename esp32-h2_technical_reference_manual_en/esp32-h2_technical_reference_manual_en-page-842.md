

```markdown
## 30.4.2 SCL and SDA Noise Filtering

SCL_Filter and SDA_Filter modules are identical and are used to filter signal noise on SCL and SDA, respectively. These filters can be enabled or disabled by configuring `I2C_SCL_FILTER_EN` and `I2C_SDA_FILTER_EN`.

Take SCL_Filter as an example. When enabled, SCL_Filter samples input signals on the SCL line continuously. These input signals are valid only if they remain unchanged for consecutive `I2C_SCL_FILTER_THRES` I2C_SCLK clock cycles. Given that only valid input signals can pass through the filter, SCL_Filter can remove glitches whose pulse width is shorter than `I2C_SCL_FILTER_THRES` I2C_SCLK clock cycles, while SDA_Filter can remove glitches whose pulse width is shorter than `I2C_SDA_FILTER_THRES` I2C_SCLK clock cycles.

## 30.4.3 SCL Clock Stretching

The I2C controller in slave mode (i.e., slave) can realize the function called clock stretching by holding the SCL line low to suspend data transmission in exchange for more time to process data. This function is enabled by setting the `I2C_SLAVE_SCL_STRETCH_EN` bit. The time period to release the SCL line from stretching is configured by the `I2C_STRETCH_PROTECT_NUM` field, in order to avoid timing sequence errors. The slave can choose to hold the SCL line low for clock stretching when one of the following four events occurs:

1. Address match: The address of the slave matches the address sent by the master via the SDA line, and the `R/W` bit is 1.
2. RAM being full: RX RAM of the slave is full. Note that when the slave receives less data than the FIFO depth, which is 32 bytes in ESP32-H2 I2C, it is not necessary to enable clock stretching; when the slave receives FIFO depth bytes or more, you may interrupt data transmission to wrapped around RAM via the FIFO threshold, or enable clock stretching for more time to process data. When clock stretching is enabled, `I2C_RX_FULL_ACK_LEVEL` must be cleared, otherwise, there will be unpredictable consequences.
3. RAM being empty: The slave is sending data, but its TX RAM is empty.
4. Sending an ACK: If `I2C_SLAVE_BYTE_ACK_CTL_EN` is set, the slave pulls SCL low when sending an ACK bit. At this stage, software validates data and configures `I2C_SLAVE_BYTE_ACK_LVL` to control the level of the ACK bit. Note that when RX RAM of the slave is full, the level of the ACK bit to be sent is determined by `I2C_RX_FULL_ACK_LEVEL`, instead of `I2C_SLAVE_BYTE_ACK_LVL`. In this case, `I2C_RX_FULL_ACK_LEVEL` should also be cleared to ensure the proper functioning of clock stretching.

When clock stretching occurs, the cause of stretching can be read from the `I2C_STRETCH_CAUSE` bit. Clock stretching can be cleared by setting the `I2C_SLAVE_SCL_STRETCH_CLR` bit.

## 30.4.4 Generating SCL Pulses in Idle State

Usually, when the I2C bus is idle, the SCL line is held high. The I2C controller in ESP32-H2 can be programmed to generate SCL pulses in an idle state. This function only works when the I2C controller is configured as master. If the `I2C_SCL_RST_SLV_EN` bit is set, hardware will send `I2C_SCL_RST_SLV_NUM` SCL pulses, and then automatically clear the `I2C_SCL_RST_SLV_EN` bit.
```