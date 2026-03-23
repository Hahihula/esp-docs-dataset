

```markdown
1. Set I2C_SCL_FORCE_OUT and I2C_SDA_FORCE_OUT, and configure GPIO_PINn_PAD_DRIVER for corresponding SCL and SDA pads as open-drain.
2. Clear I2C_SCL_FORCE_OUT and I2C_SDA_FORCE_OUT.

Because these lines are configured as open-drain, the low-to-high transition time of each line is longer, determined together by the pull-up resistor and line capacitance. The output duty cycle of I2C is limited by the SDA and SCL line's pull-up speed, mainly SCL's speed.

In addition, when I2C_SCL_FORCE_OUT and I2C_SCL_PD_EN are set to 1, SCL can be forced low; when I2C_SDA_FORCE_OUT and I2C_SDA_PD_EN are set to 1, SDA can be forced low.
```

## 29.4.7 Timing Parameter Configuration

Figure 29.4-1 shows the timing diagram of an I2C master. This figure also specifies registers used to configure the START bit, STOP bit, data hold time, data sample time, waiting time on the rising SCL edge, etc. Timing parameters are calculated as follows in I2C_SCLK clock cycles:

```markdown
1.  tLOW = (I2C_SCL_LOW_PERIOD + 1) · TI2CSCLK

2.  tHIGH = (I2C_SCL_HIGH_PERIOD + 1) · TI2CSCLK

3.  tsU:STA = (I2C_SCL_RST_START_SETUP_TIME + 1) · TI2CSCLK

4.  tHD:STA = (I2C_SCL_START_HOLD_TIME + 1) · TI2CSCLK

5.  tr = (I2C_SCL_WAIT_HIGH_PERIOD + 1) · TI2CSCLK

6.  tsU:STO = (I2C_SCL_STOP_SETUP_TIME + 1) · TI2CSCLK

7.  tBUF = (I2C_SCL_STOP_HOLD_TIME + 1) · TI2CSCLK

8.  tHD:DAT = (I2C_SDA_HOLD_TIME + 1) · TI2CSCLK

9.  tsU:DAT = (I2C_SCL_LOW_PERIOD - I2C_SDA_HOLD_TIME) · TI2CSCLK
```

Timing registers below are divided into two groups, depending on the mode in which these registers are active:

- Master mode only:
```