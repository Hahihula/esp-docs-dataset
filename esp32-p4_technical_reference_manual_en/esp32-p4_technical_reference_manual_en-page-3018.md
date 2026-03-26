

```markdown
Chapter 61 Temperature Sensor (TSENS)
GoBack

Register 61.2. TSENS_CTRL2_REG (0x0004)

TSens_XPD_WAIT Configures the wait time (in clock cycles) for the sensor to release from reset.
(R/W)

TSens_XPD_FORCE Configures whether to enable force power up/down the temperature sensor.
0: Disable force power up function
1: Disable force power down function
2: Enable force power up temperature sensor
3: Enable force power down temperature sensor
(R/W)

TSens_CLK_INV Configures the phase of the temperature sensor clock. (R/W)

Register 61.3. TSENS_INT_RAW_REG (0x0008)

TSens_COCPU_TSENS_WAKE_INT_RAW The raw interrupt status of the TSENS_COCPU_TSENS_WAKE_INT. (R/WTC/SS)
```