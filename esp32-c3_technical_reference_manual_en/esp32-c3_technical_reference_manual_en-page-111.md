
```markdown
## 4.3.4 eFuse VDDQ Timing

The eFuse Controller operates with 20 MHz of clock frequency, and its programming voltage VDDQ should be configured as follows:

*   **EFUSE_DAC_NUM** (the rising period of VDDQ): The default value of VDDQ is 2.5 V and the voltage increases by 0.01 V in each clock cycle. Thus, the default value of this parameter is 255;
*   **EFUSE_DAC_CLK_DIV** (the clock divisor of VDDQ): The clock period to program VDDQ should be larger than 1 µs;
*   **EFUSE_PWR_ON_NUM** (the power-up time for VDDQ): The programming voltage should be stabilized after this time, which means the value of this parameter should be configured to exceed the result of EFUSE_DAC_CLK_DIV times EFUSE_DAC_NUM;
*   **EFUSE_PWR_OFF_NUM** (the power-out time for VDDQ): The value of this parameter should be larger than 10 µs.

Table 4.3-5. Configuration of Default VDDQ Timing Parameters

| EFUSE_DAC_NUM | EFUSE_DAC_CLK_DIV | EFUSE_PWR_ON_NUM | EFUSE_PWR_OFF_NUM |
|---------------|-------------------|------------------|-------------------|
| 0xFF          | 0x28              | 0x3000           | 0x190             |

## 4.3.5 The Use of Parameters by Hardware Modules

Some hardware modules are directly connected to the eFuse peripheral in order to use the parameters listed in Table 4.3-1 and Table 4.3-3, specifically those marked with "Y" in columns "Accessible by Hardware". Users cannot intervene in this process.

## 4.3.6 Interrupts

*   **PGM_DONE interrupt**: Triggered when eFuse programming has finished. To enable this interrupt, set the EFUSE_PGM_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1;
*   **READ_DONE interrupt**: Triggered when eFuse reading has finished. To enable this interrupt, set the EFUSE_READ_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1.
```