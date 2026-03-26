

```markdown
## Register 45.2. ANA_I2C_MST_I2C1_CTRL_REG (0x0004)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | 0                            |
| 29  | 0                            |
| 28  | 0                            |
| 27  | 0                            |
| 26  | 0                            |
| 25  | 0                            |
| 24  | 0                            |
|     | Reset                        |

**ANA_I2C_MST_I2C1_CTRL** Configures the transmission information for I2C1. Its subfields have the same meaning with ANA_I2C_MST_I2C0_CTRL. (R/W)

**ANA_I2C_MST_I2C1_BUSY** Represents whether I2C1 is currently transferring data
- 0: I2C1 is not transferring data
- 1: I2C1 is transferring data
(R/O)
```

```markdown
## Register 45.3. ANA_I2C_MST_ANA_CONF2_REG (0x0020)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 30  | 0                            |
| 29  | 0                            |
| 28  | 0                            |
| 27  | 0                            |
| 26  | 0                            |
| 25  | 0                            |
| 24  | 0                            |
|     | Reset                        |

**ANA_I2C_MST_ANA_CONF2** Configures which I2C master the following analog modules uses. If the corresponding bit is set to 1, I2CO master is used for communication; if set to 0, I2C1 master is used. Since the slave address has already been defined, erroneous communication will not be caused.

Bit5: SYS_PLL  
Bit6: SDIO_PLL  
Bit7: ANA_SENSOR  
Bit8: PLLA  
Bit9: MSPI  
Bit10: DIG_REG  
Bit11: CPU_PLL  
Bit12: BIAS  
(R/W)
```