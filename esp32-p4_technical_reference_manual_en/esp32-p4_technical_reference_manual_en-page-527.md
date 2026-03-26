

```markdown
Register 8.33. EFUSE_DAC_CONF_REG (0x01EB)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 18  | EFUSE_OE_CLR                                                                |
| 17  |                                                                             |
| 16  | EFUSE_DAC_NUM                                                               |
| 9   | EFUSE_DAC_CLK_PAD_SEL                                                       |
| 8   | EFUSE_DAC_CLK_DIV                                                           |
| 7   |                                                                             |
| 0   | Reset                                                                      |

EFUSE_DAC_CLK_DIV Configures the division factor of the rising clock of the programming voltage. (R/W)

EFUSE_DAC_CLK_PAD_SEL Don't care. (R/W)

EFUSE_DAC_NUM Configures clock cycles for programming voltage to rise. Measurement unit: a clock cycle divided by EFUSE_DAC_CLK_DIV. (R/W)

EFUSE_OE_CLR Configures whether to reduce the power supply of the programming voltage.
0: Not reduce.
1: Reduce.
(R/W)
```

```markdown
Register 8.34. EFUSE_RD_TIM_CONF_REG (0x01EC)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 24  | EFUSE_READ_INIT_NUM                                                         |
| 23  |                                                                             |
| 16  | EFUSE_TSUR_A                                                                |
| 15  |                                                                             |
| 8   | EFUSE_TRD                                                                   |
| 7   |                                                                             |
| 0   | Reset                                                                      |

EFUSE_THR_A Configures the read hold time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_TRD Configures the read time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_TSUR_A Configures the read setup time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_READ_INIT_NUM Configures the waiting time of reading eFuse memory. Measurement unit: One cycle of the eFuse core clock. (R/W)
```