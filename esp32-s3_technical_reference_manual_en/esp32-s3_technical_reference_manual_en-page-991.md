**Title: Chapter 27 I2C Controller (I2C)**

---

1. Set `I2C_SCL FORCE_OUT` and `I2C_SDA FORCE_OUT`, and configure `GPIO_PIN PAD_DRIVER` for corresponding SCL and SDA pads as open-drain.

2. Clear `I2C_SCL FORCE_OUT` and `I2C_SDA FORCE_OUT`.

Because these lines are configured as open-drain, the low-to-high transition time of each line is longer, determined together by the pull-up resistor and line capacitance. The output duty cycle of I2C SDA and SCL line's pull-up speed, mainly SCL’s speed.

In addition, when `I2C_SCL FORCE_OUT` and `I2C_SDA PD_EN` are set to 1, SCL can be forced low; when `I2C_SCL FORCE_OUT` and `I2C_SDA PD_EN` are set to 1, SDA can be forced low.

---

**Subtitle: Timing Parameter Configuration**

**Figure Caption:** Figure 27.4-1. I2C Timing Diagram

**Body Text:**
Figure 27.4-1 shows the timing diagram of an I2C master. This figure also specifies registers used to configure the START bit, STOP bit, data hold time, data sample time, waiting time on the rising SCL edge, etc. Timing parameters are calculated as follows in `I2C_SCL` clock cycles:

1. \( t_{LOW} = (I2C_SCL_LOW_PERIOD + 1) \cdot T_{I2C_SCLK} \)
2. \( t_{HIGH} = (I2C_SCL_HIGH_PERIOD + 1) \cdot T_{I2C_SCLK} \)
3. \( t_{SU:STA} = (I2C_SCL_RSTART_SETUP_TIME + 1) \cdot T_{I2C_SCLK} \)
4. \( t_{HD:STA} = (I2C_SCL_STSTART_HOLD_TIME + 1) \cdot T_{I2C_SCLK} \)
5. \( t_r = (I2C_SCL_WAIT_HIGH_PERIOD + 1) \cdot T_{I2C_SCLK} \)
6. \( t_{SU:STO} = (I2C_SCL_STOP_SETUP_TIME + 1) \cdot T_{I2C_SCLK} \)
7. \( t_{BUF} = (I2C_SCL_STHOLD_TIME + 1) \cdot T_{I2C_SCLK} \)
8. \( t_{HD:DAT} = (I2C_SCL_HLD_TIME + 1) \cdot T_{I2C_SCLK} \)
9. \( t_{SU:DAT} = (I2C_SCL_LOW_PERIOD - I2C_SDA_HOLD_TIME) \cdot T_{I2C_SCL} \)

Timing registers below are divided into two groups, depending on the mode in which these registers are active:

- Master mode only.

---

**Footer:**  
Espressif Systems  
991 ESP32-S3 TRM (Version 1.7)  

**Menu Options:**
- Submit Documentation
- Feedback

**Navigation Link:** GoBack