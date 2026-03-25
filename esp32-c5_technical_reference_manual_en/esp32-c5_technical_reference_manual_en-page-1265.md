

```markdown
Register 34.50. LP_I2C_SCL_SP_CONF_REG (0x0080)
```

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | Reset |

LP_I2C_SCL_RST_SLV_EN Configures to send out SCL pulses when I2C master is IDLE. The number of pulses equals to LP_I2C_SCL_RST_SLV_NUM. (R/W/SC)

LP_I2C_SCL_RST_SLV_NUM Configure the pulses of SCL generated in I2C master mode.

Valid when LP_I2C_SCL_RST_SLV_EN is 1.
Measurement unit: I2C_SCL_K clock cycles
(R/W)

LP_I2C_SCL_PD_EN Configures to power down the I2C output SCL line.
0: Not power down
1: Not work and power down
Valid only when LP_I2C_SCL_FORCE_OUT is 1
(R/W)

LP_I2C_SDA_PD_EN Configures to power down the I2C output SDA line.
0: Not power down.
1: Not work and power down.
Valid only when LP_I2C_SDA_FORCE_OUT is 1. (R/W)
```