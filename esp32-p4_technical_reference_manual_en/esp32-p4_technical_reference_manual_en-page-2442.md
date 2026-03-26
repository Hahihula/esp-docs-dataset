

# 45.6 Register Summary

The addresses in this section are relative to Analog I2C Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers** | | | |
| ANA_I2C_MST_I2CO_CTRL_REG | I2CO transmission configuration register | 0x0000 | varies |
| ANA_I2C_MST_I2C1_CTRL_REG | I2C1 transmission configuration register | 0x0004 | varies |
| ANA_I2C_MST_ANA_CONF2_REG | I2C master selection register | 0x0020 | varies |
| ANA_I2C_MST_I2CO_CTRL1_REG | I2CO transmission rate and signal phase configuration register | 0x0024 | R/W |
| ANA_I2C_MST_I2C1_CTRL1_REG | I2C1 transmission rate and signal phase configuration register | 0x0028 | R/W |
| ANA_I2C_MST_DATE_REG | Version control register | 0x0038 | R/W |