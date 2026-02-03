**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Section Header:**
17.4 Register Summary

**Body Text:**
In this section, the addresses of all the registers starting with SYSTEM are relative to the base address of system registers provided in Table 4.3-3 in Chapter 4 System and Memory; and those starting with APB are relative to the base address of APB control also provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table:**
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SYSTEM\Core_1_Control_0_Reg | Core1 control register 0 | 0x0000 | R/W |
| SYSTEM\Core_1_Control_1_Reg | Core1 control register 1 | 0x0004 | R/W |
| SYSTEM\CPU_Per_Conf_Reg | CPU peripheral clock configuration register | 0x0010 | R/W |
| SYSTEM\Perip_Clk_Eno_Reg | System peripheral clock enable register 0 | 0x0018 | R/W |
| SYSTEM\Perip_Clk_Eni_Reg | System peripheral clock enable register 1 | 0x001C | R/W |
| SYSTEM\Perip_Rst_Emo_Reg | System peripheral reset register 0 | 0x0020 | R/W |
| SYSTEM\Perip_Rst_Emi_Reg | System peripheral reset register 1 | 0x0024 | R/W |
| SYSTEM\BT_Lpck_Div_Frac_Reg | Low-power clock configuration register 1 | 0x002C | R/W |
| SYSTEM\CPU_Intr_From_Cpu_0_Reg | Software interrupt source register 0 | 0x0030 | R/W |
| SYSTEM\CPU_Intr_From_Cpu_1_Reg | Software interrupt source register 1 | 0x0034 | R/W |
| SYSTEM\CPU_Intr_From_Cpu_2_Reg | Software interrupt source register 2 | 0x0038 | R/W |
| SYSTEM\CPU_Intr_From_Cpu_3_Reg | Software interrupt source register 3 | 0x003C | R/W |
| SYSTEM\RSA_Pd_Ctrl_Reg | RSA memory power control register | 0x0040 | R/W |
| SYSTEM\Edma_Ctrl_Reg | EDMA control register | 0x0044 | R/W |
| SYSTEM\Cache_Control_Reg | Cache control register | 0x0048 | R/W |
| SYSTEM\External_Device_Encrypt_Decrypt_Control_Reg | External memory encryption and decryption control register | 0x004C | R/W |
| SYSTEM\RTC_Fastmem_Conf_Reg | Fast memory CRC configuration register | 0x0050 | varies |
| SYSTEM\RTC_Fastmem_Crc_Reg | Fast memory CRC result register | 0x0054 | RO |
| SYSTEM\Clock_Gate_Reg | System clock control register | 0x005C | R/W |
| SYSTEM\Sysclk_Conf_Reg | System clock configuration register | 0x0060 | varies |
| SYSTEM\Date_Reg | Version register | 0x0FFC | R/W |

**Additional Table:**
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SYSCON_Clkgate_Force_On_Reg | Internal memory clock gate enable register | 0x00A8 | R/W |
| SYSCON_Mem_Power_Down_Reg | Internal memory control register | 0x00AC | R/W |
| SYSCON_Mem_Power_Up_Reg | Internal memory control register | 0x00BO | R/W |

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)