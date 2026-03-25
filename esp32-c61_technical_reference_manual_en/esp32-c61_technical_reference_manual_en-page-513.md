

```markdown
| Name                                       | Description                                                                                                                                              | Address   | Access |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_IMM_SLEEP_SYSCLK_REG                  | Software-controlled enable signal for system root clk switching during sleep                                                                            | 0xOOD0    | WT     |
| PMU_IMM_HP_FUNC_ICG_REG                   | Software-controlled configuration for functional clock gating of PMU's forced update output                                                               | 0xOOD4    | WT     |
| PMU_IMM_HP_APB_ICG_REG                    | Software-controlled configuration for APB clock gating of PMU's forced update output                                                                     | 0xOOD8    | WT     |
| PMU_IMM_MODEM_ICG_REG                     | Software-controlled configuration for HP system Modem clock gating of PMU's forced update output                                                          | 0xODC     | WT     |
| PMU_IMM_PAD_HOLD_ALL_REG                  | Software-controlled signal to tie PMU's HP/LP GPIOs HOLD high or low                                                                                      | 0xOE4     | WT     |
| PMU_IMM_I2C_ISO_REG                       | Software-controlled signal to tie PMU's i2c iso enable high or low                                                                                        | 0xOE8     | WT     |
| PMU_POWER_WAIT_TIMER0_REG                 | Software-controlled power-on/off waiting timer for PMU                                                                                                     | 0xOEC     | R/W    |
| PMU_POWER_WAIT_TIMER1_REG                 | Software-controlled power-on/off waiting timer for LP PERI controlled by PMU                                                                             | 0xOF0     | R/W    |
| PMU_POWER_WAIT_TIMER2_REG                 | Software-controlled waiting timer for HP, LP ISO and reset in PMU                                                                                          | 0xOF4     | R/W    |
| PMU_POWER_PD_TOP_CNTL_REG                 | Configuration register for "Peripherals+ROM" power domain controlled by PMU                                                                             | 0xOF8     | R/W    |
| PMU_POWER_PD_HPAON_CNTL_REG               | Configuration register for Modem Power power domain controlled by PMU                                                                                     | 0xOFc     | R/W    |
| PMU_POWER_PD_HPCPU_CNTL_REG               | Configuration register for CPU power domain controlled by PMU                                                                                            | 0x100     | R/W    |
| PMU_POWER_PD_HPWI_FI_CNTL_REG             | Configuration register for MODEM power domain controlled by PMU                                                                                           | 0x108     | R/W    |
| PMU_POWER_PD_LPPERI_CNTL_REG              | Configuration register for LPSYS_OFF power domain controlled by PMU                                                                                       | 0x10C     | R/W    |
| PMU_POWER_PD_MEM_CNTL_REG                 | Configuration register for Internal SRAMx power domain's ISO and overall switch controlled by PMU                                                         | 0x110     | R/W    |
| PMU_POWER_PD_MEM_MASK_REG                 | Configuration register for LDO switch of individual Internal SRAMx power supply controlled by PMU                                                          | 0x114     | R/W    |
| PMU_POWER_HP_PAD_REG                      | Configuration register for HP GPIOs power supply controlled by PMU                                                                                         | 0x118     | R/W    |
| PMU_POWER_VDD_SPI_CNTL_REG                | Configuration register for VDD_SPI power supply controlled by PMU                                                                                        | 0x11C     | R/W    |
```