

```markdown
Chapter 45 Analog I2C Controller

GoBack

Figure 45.4-1. Signal Phase

Operation in Sleep Modes

In chip sleep modes, the operation of the Analog I2C Controller can be driven by the Low-Power CPU (see Chapter 3 Low-Power CPU).

Dual Master Operation Mode

The module integrates two independent master modules, each with its own set of configurations. The two masters can operate independently, configuring different analog modules, thereby improving operational efficiency.

45.5 Programming Procedures

The following is the process for configuring analog modules using the Analog I2C Controller.

* Write 1 to LPPERI_CK_EN_LP_I2CMST to enable the clock of the Controller.
* Configure ANA_I2C_MST_ANA_CONF2 to select the module for communication.
* Configure ANA_I2C_MST_I2Cx_SDA_SIDE_GUARD and ANA_I2C_MST_I2Cx_SCL_PULSE_DUR to determine the transmission rate and signal phase of the I2C signal.
* Configure ANA_I2C_MST_I2Cx_CTRL to select relevant information for the current communication.
* Read ANA_I2C_MST_I2Cx_BUSY. A low state indicates the end of the current communication for I2Cx.

Espressif Systems

2441
ESP32-P4 TRM
PRELIMINARY
```