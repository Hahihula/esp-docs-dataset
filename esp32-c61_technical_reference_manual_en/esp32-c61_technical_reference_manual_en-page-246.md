

```markdown
Register 5.34. EFUSE_DAC_CONF_REG (0x01EB)

EFUSE_DAC_CLK_DIV Controls the division factor of the rising clock of the programming voltage.
(R/W)

EFUSE_DAC_CLK_PAD_SEL Reserved (R/W)

EFUSE_DAC_NUM Controls the rising period of the programming voltage.
Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_OE_CLR Reduces the power supply of the programming voltage. (R/W)
```

```markdown
Register 5.35. EFUSE_RD_TIM_CONF_REG (0x01EC)

EFUSE_THR_A Configures the read hold time.
Measurement unit: One cycle of the eFuse core clock.(R/W)

EFUSE_TRD Configures the read time.
Measurement unit: One cycle of the eFuse core clock.(R/W)

EFUSE_TSUR_A Configures the read setup time.
Measurement unit: One cycle of the eFuse core clock.(R/W)

EFUSE_READ_INIT_NUM Configures the waiting time of reading eFuse memory.
Measurement unit: One cycle of the eFuse core clock. (R/W)
```