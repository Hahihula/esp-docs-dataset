Title: Chapter 5 eFuse Controller

Body Text:
During the chip boot process, eFuse controller will update eFuse data into registers which can be accessed by users automatically. You can get programmed eFuse data by reading corresponding registers. Thus, it is no need to update eFuse read registers in such case.

Subtitle: 5.3.4 eFuse VDDQ Timing

Body Text:
The eFuse Controller operates with 20 MHz, one cycle is 50 ns, and its programming voltage VDDQ should be configured as follows:

- EFUSE_DAC_NUM (store the rising period of VDDQ): The default value of VDDQ is 2.5 V and the voltage increases by 0.01 V in each clock cycle. Thus, the default value of this parameter is 255;
- EFUSE_DAC_CLK_DIV (the clock divisor of VDDQ): The clock period to program VDDQ should be larger than 1 µs;
- EFUSE_PWR_ON_NUM (the power-up time for VDDQ): The programming voltage should be stabilized after this time, which means the value of this parameter should be configured to exceed the value of EFUSE_DAC_CLK_DIV multiply by EFUSE_DAC_NUM;
- EFUSE_PWR_OFF_NUM (the power-out time for VDDQ): The value of this parameter should be larger than 10 µs.

Table:
| EFUSE_DAC_NUM | EFUSE_DAC_CLK_DIV | EFUSE_PWR_ON_NUM | EFUSE_PWR_OFF_NUM |
|----------------|--------------------|-------------------|--------------------|
| OxFF           | 0x28               | 0x3000            | 0x190             |

Caption for Table:
Table 5.3-5. Configuration of Default VDDQ Timing Parameters

Subtitle: 5.3.5 The Use of Parameters by Hardware Modules

Body Text:
Some hardware modules are directly connected to the eFuse peripheral in order to use the parameters listed in Table 5.3-1 and Table 5.3-3, specifically those marked with “Y” in columns “Accessible by Hardware”. Users cannot intervene in this process.

Subtitle: 5.3.6 Interrupts

Body Text:
- PGM_DONE interrupt: Triggered when eFuse programming has finished. Set EFUSE_PGM_DONE_INT_ENA to enable this interrupt;
- READ_DONE interrupt: Triggered when eFuse reading has finished. Set EFUSE_READ_DONE_INT_ENA to enable this interrupt.

Footer Information:
Espressif Systems
422 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

Navigation Link at the top right corner of page image is "GoBack".