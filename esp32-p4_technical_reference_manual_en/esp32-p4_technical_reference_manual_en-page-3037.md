

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LPADC_MEAS1_CTRL2_REG                     | LP ADC1 configuration registers.                                            | 0x000C    | varies |
| LPADC_MEAS1_MUX_REG                       | LP or HP ADC controller selection register for SAR ADC1.                    | 0x0010    | R/W    |
| LPADC_ATTEN1_REG                          | LP ADC1 attenuation registers.                                              | 0x0014    | R/W    |
| LPADC_READER2_CTRL_REG                    | LP ADC2 Reader control register.                                            | 0x0024    | R/W    |
| LPADC_MEAS2_CTRL2_REG                     | LP ADC2 configuration registers.                                            | 0x0030    | varies |
| LPADC_MEAS2_MUX_REG                       | LP or HP controller selection register for SAR ADC2.                        | 0x0034    | R/W    |
| LPADC_ATTEN2_REG                          | LP ADC2 attenuation registers.                                              | 0x0038    | R/W    |

LP ADC Power Control Registers
-------------------------------
| LPADC_FORCE_WPD_SAR_REG                  | LP ADC Controllers power control registers.                                 | 0x003C    | R/W    |

LP ADC Interrupt Registers
---------------------------
| LPADC_COCPU_INT_RAW_REG                  | Raw register of LP ADC interrupts.                                          | 0x0048    | R/WTC/SS |
| LPADC_INT_ENA_REG                         | Enable register of LP ADC interrupts.                                       | 0x004C    | R/WTC  |
| LPADC_INT_ST_REG                          | Status register of LP ADC interrupts.                                       | 0x0050    | RO     |
| LPADC_INT_CLR_REG                         | Clear register of LP ADC interrupts.                                        | 0x0054    | WT     |
| LPADC_INT_ENA_W1TS_REG                   | LPADC_INT_ENA_REG configuration register.                                  | 0x0058    | WT     |
| LPADC_INT_ENA_W1TC_REG                   | LPADC_INT_ENA_REG configuration register.                                  | 0x005C    | WT     |

LP ADC Wake-up Control Registers
---------------------------------
| LPADC_WAKEUP1_REG                        | LP ADC1 wake-up configuration registers.                                    | 0x0060    | varies |
| LPADC_WAKEUP2_REG                         | LP ADC2 wake-up configuration registers.                                   | 0x0064    | varies |
| LPADC_WAKEUP_SEL_REG                      | Wake-up source selection register.                                         | 0x0068    | R/W    |
| LPADC_SAR1_HW_WAKEUP_REG                 | LP ADC1 automatic monitoring configuration registers.                      | 0x006C    | R/W    |
| LPADC_SAR2_HW_WAKEUP_REG                 | LP ADC2 automatic monitoring configuration registers.                      | 0x0070    | R/W    |
```