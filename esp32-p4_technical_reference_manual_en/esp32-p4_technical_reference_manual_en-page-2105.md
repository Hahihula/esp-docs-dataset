

# 41.7 Register Summary

The addresses in this section are relative to VAD base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **VAD Registers** | | | |
| LP_I2S_VAD_CONF_REG | Operation control register | 0x0000 | varies |
| LP_I2S_VAD_RESULT_REG | Voice activity status register | 0x0004 | RO |
| LP_I2S_VAD_PARAMO_REG | Parameter configuration register 0 | 0x0080 | R/W |
| LP_I2S_VAD_PARAM1_REG | Parameter configuration register 1 | 0x0084 | R/W |
| LP_I2S_VAD_OBO_REG | Status register for key operational variables | 0x00B0 | RO |