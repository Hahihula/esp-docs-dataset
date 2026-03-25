

```markdown
2. Configure the Interrupt Matrix to enable the CPU to respond to eFuse interrupt signals. See Chapter 9 Interrupt Matrix.
3. Wait for the PGM_DONE or READ_DONE interrupt.
4. Set bit I/O in register EFUSE_INT_CLR_REG to 1 to clear the PGM_DONE or READ_DONE interrupt.

Note

When eFuse controller is updating its registers, it will use EFUSE_PGM_DATA[n_REG] (n=0, 1, ..., 7) again to store data. So please do not write important data into these registers before this updating process is initiated.

During the chip boot process, eFuse controller will automatically update data from eFuse memory into the registers that can be accessed by users. Users can get programmed eFuse data by reading corresponding registers. Thus, there is no need to update the reading data registers in such case.

5.4.3 eFuse VDDQ Timing

The eFuse controller operates at the clock frequency of 20 MHz, and its programming voltage VDDQ should be configured as follows:

*   EFUSE_DAC_NUM (the rising period of VDDQ): The default value of VDDQ is 2.5 V and the voltage increases by 0.01 V in each clock cycle. The default value of this parameter is 255.
*   EFUSE_DAC_CLK_DIV (the clock divisor of VDDQ): The clock period to program VDDQ should be larger than 1 µs.
*   EFUSE_PWR_ON_NUM (the power-up time for VDDQ): The programming voltage should be stabilized after this time, which means the value of this parameter should be configured to exceed the result of EFUSE_DAC_CLK_DIV times EFUSE_DAC_NUM.
*   EFUSE_PWR_OFF_NUM (the power-out time for VDDQ): The value of this parameter should be larger than 10 µs.

Table 5.4-2. Configuration of Default VDDQ Timing Parameters

| EFUSE_DAC_NUM | EFUSE_DAC_CLK_DIV | EFUSE_PWR_ON_NUM | EFUSE_PWR_OFF_NUM |
|---------------|-------------------|------------------|-------------------|
| 0xFF          | 0x28              | 0x3000           | 0x190             |

5.4.4 Parameters Used by Hardware Modules

Some hardware modules are directly connected to the eFuse peripheral in order to use the parameters that are marked with “Y” in columns “Accessible by Hardware” of Table 5.3-1 and Table 5.3-3. Users cannot intervene in this process.

5.5 Interrupts

*   PGM_DONE interrupt: Triggered when eFuse programming has finished. To enable this interrupt, set the EFUSE_PGM_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1.
*   READ_DONE interrupt: Triggered when eFuse reading has finished. To enable this interrupt, set the EFUSE_READ_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1.
```