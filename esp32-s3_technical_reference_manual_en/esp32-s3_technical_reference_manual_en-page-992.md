Title: Chapter 27 I2C Controller (I2C)

1. **I2C_SCL_START_HOLD_TIME**: Specifies the interval between pulling SDA low and pulling SCL low when the master generates a START condition. This interval is (I2C_SCL_START_HOLD_TIME + 1) in I2C_SCL_cycles. This register is active only when the I2C controller works in master mode.

2. **I2C_SCL_LOW_PERIOD**: Specifies the low period of SCL. This period lasts (I2C_SCL_LOW_PERIOD + 1) in I2C_SCL_cycles. However, it could be extended when SCL is pulled low by peripheral devices or by an END command executed by the I2C controller, or when the clock is stretched. This register is active only when the I2C controller works in master mode.

3. **I2C_SCL_WAIT_HIGH_PERIOD**: Specifies time for SCL to go high within 12C_SCL_cycles. Please make sure that SCL could be pulled high within this time period. Otherwise, the high period of SCL may be incorrect. This register is active only when the I2C controller works in master mode.

4. **I2C_SCL_HIGH_PERIOD**: Specifies the high period of SCL in 12C_SCL_cycles. This register is active only when the I2C controller works in master mode. When SCL goes high within (I2C_SCL_WAIT_HIGH_PERIOD + 1) in 12C_SCL_cycles, its frequency is:

   \[ f_{ scl } = \frac{f_{i2c_scl}}{I2C_SCL_LOW_PERIOD + I2C_SCL_HIGH_PERIOD + I2C_SCL_WAIT_HIGH_PERIOD+3} \]

Master mode and slave mode:
   
1. **I2C_SDA_SAMPLE_TIME**: Specifies the interval between the rising edge of SCL and the level sampling time of SDA. It is advised to set a value in the middle of SCL’s high period, so as to correctly sample the I2C level signal. This register is active both in master mode and slave mode.

2. **I2C_SDA_HOLD_TIME**: Specifies the interval between changing the SDA output level and the falling edge of SCL. This register is active also be in master mode and slave mode.

Timing parameters limits corresponding register configuration:

1. \[ \frac{f_{ scl_sck }}{f_{scl}} > 20 \]

2. \(3 \times f_{I2C_SCL} < ( I2C_SDA_HOLD_TIME - 4 ) \times f_{APB_CLK}\)

3. **I2C_SCL_HOLD_TIME + I2C_SCL_START_HOLD_TIME > SDA_FILTERThRES + 3**

4. **I2C_SCL_WAIT_HIGH_PERIOD < I2C_SDA_SAMPLE_TIME < I2C_SCL_HIGH_PERIOD < I2C_SCL_START_HOLD_TIME + I2C_SCL_RSTART_SETUP_TIME**

5. \[ I2C_SCL_STRETCH_PROTECT_NUM > I2C_SCL_HOLD_TIME > I2C_SCL_LOW_PERIOD\]

Subtitle: 27.4.8 Timeout Control

The I2C controller has three types of timeout control, namely timeout control for SCL FSM, for SCL_MAIN_FSM, and for the SCL line. The first two are always enabled, while the third is configurable.

When SCL FSM remains unchanged for more than \(I2C_SCL_ST_TO_I2C\) clock cycles, an I2C_SCL_ST_TO_INT interrupt is triggered, and then SCL FSM goes to idle state. The value of \[ I2C_SCL_ST_TO_I2C\] should be less than or equal to 22, which means SCL FSM could remain unchanged for \(I2C_SCL\) clock cycles at most before the interrupt is generated.

When SCL MAIN FSM remains unchanged for more than (I2C_SCL_MAIN_TO_I2C) I2C_SCL clock cycles,

Footer: Espressif Systems  
Page Number and Document Information:
- Page 992
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback