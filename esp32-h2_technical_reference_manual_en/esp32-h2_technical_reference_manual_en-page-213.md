

```markdown
Register 5.110. EFUSE_INT_CLR_REG (0x01E4)

EFUSE_READ_DONE_INT_CLR Write 1 to clear read_done interrupt. (WO)
EFUSE_PGM_DONE_INT_CLR Write 1 to clear pgm_done interrupt. (WO)


Register 5.111. EFUSE_DAC_CONF_REG (0x01E8)

EFUSE_DAC_CLK_DIV Configures the division factor of the rising clock of the programming voltage.
(R/W)

EFUSE_DAC_CLK_PAD_SEL Don't care. (R/W)

EFUSE_DAC_NUM Configures the rising period of the programming voltage. Measurement unit:
Divided clock frequency by EFUSE_DAC_CLK_DIV. (R/W)

EFUSE_OE_CLR Reduces the power supply of the programming voltage. (R/W)
```