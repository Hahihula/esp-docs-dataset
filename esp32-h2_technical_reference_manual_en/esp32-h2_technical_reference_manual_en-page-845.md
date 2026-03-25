

```markdown
1. Set `I2C_SCL_FORCE_OUT` and `I2C_SDA_FORCE_OUT`, and configure `GPIO_PINn_PAD_DRIVER` for corresponding SCL and SDA pads as open-drain.
2. Clear `I2C_SCL_FORCE_OUT` and `I2C_SDA_FORCE_OUT`.

Because these lines are configured as open-drain, the low-to-high transition time of each line is longer, determined together by the pull-up resistor and line capacitance. The output duty cycle of I2C is limited by the SDA and SCL line's pull-up speed, mainly SCL's speed.

In addition, when `I2C_SCL_FORCE_OUT` and `I2C_SCL_PD_EN` are set to 1, SCL can be forced low; when `I2C_SDA_FORCE_OUT` and `I2C_SDA_PD_EN` are set to 1, SDA can be forced low.

## 30.4.7 Timing Parameter Configuration

Figure 30.4-1 shows the timing diagram of an I2C master. This figure also specifies registers used to configure the START bit, STOP bit, data hold time, data sample time, waiting time on the rising SCL edge, etc. Timing parameters (please refer to Table 30.3-1) are calculated as follows in `I2C_SCL` clock cycles:

1. `t_LOW = (I2C_SCL_LOW_PERIOD + 1) · T_I2C_SCLK`
2. `t_HIGH = (I2C_SCL_HIGH_PERIOD + 1) · T_I2C_SCLK`
3. `t_SU:STA = (I2C_SCL_RST_START_SETUP_TIME + 1) · T_I2C_SCLK`
4. `t_HD:STA = (I2C_SCL_START_HOLD_TIME + 1) · T_I2C_SCLK`
5. `t_r = (I2C_SCL_WAIT_HIGH_PERIOD + 1) · T_I2C_SCLK`
6. `t_SU:STO = (I2C_SCL_STOP_SETUP_TIME + 1) · T_I2C_SCLK`
7. `t_BUF = (I2C_SCL_STOP_HOLD_TIME + 1) · T_I2C_SCLK`
8. `t_HD:DAT = (I2C_SDA_HOLD_TIME + 1) · T_I2C_SCLK`
9. `t_SU:DAT = (I2C_SCL_LOW_PERIOD – I2C_SDA_HOLD_TIME) · T_I2C_SCLK`

Timing registers below are divided into two groups, depending on the mode in which these registers are active:

* Master mode only:
```