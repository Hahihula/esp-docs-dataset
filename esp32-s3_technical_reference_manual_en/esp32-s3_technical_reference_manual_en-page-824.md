**Chapter Title:**
- Chapter 17 System Registers (SYSTEM)

**Section Titles and Content:**

1. **17.3.1.2 External Memory**
   - SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG configures encryption and decryption options of the external memory.
   - For details, please refer to Chapter 23 External Memory Encryption and Decryption (XTS_AES).

2. **17.3.1.3 RSA Memory**
   - SYSTEM_RSA_PD_CTRL_REG controls the SRAM memory in the RSA accelerator:
     - Setting the SYSTEM_RSA_MEM_PD bit to send the RSA memory into retention state.
       This bit has the lowest priority, meaning it can be masked by the SYSTEM_RSA_MEMFORCE_PU field.
       This bit is invalid when the Digital Signature (DS) occupies the RSA.
     - Setting the SYSTEM_RSA_MEM FORCE PU bit to force the RSA memory to work as normal when the chip enters light sleep:
       This bit has the second highest priority, meaning it overrides the SYSTEM_RSA_MEM_PD field.
     - Setting the SYSTEM_RSA_MEM FORCE_PD bit to send the RSA memory into retention state. 
       This bit has the highest priority, meaning it sends the RSA memory into retention state regardless of the SYSTEM_RSA_MEMFORCE_PU field.

3. **17.3.2 Clock Registers**
   - The following registers are used to set clock sources and frequency.
     For more information, please refer to Chapter 7 Reset and Clock:
       - SYSTEM_CPU_PER_CONF_REG
       - SYSTEM_SYSLCK_CONF_REG
       - SYSTEM_BT_LPCK_DIV_FRAC_REG

4. **17.3.3 Interrupt Signal Registers**
   - The following registers are used for generating the interrupt signals,
     which then can be routed to the CPU peripheral interrupts via the interrupt matrix.
     To be more specific, writing 1 to any of the following registers generates an interrupt signal:
     Therefore, these registers can be used by software to control interrupts. For more information, please refer to Chapter 9 Interrupt Matrix (INTERRUPT):
       - SYSTEM_CPU_INTEFROM_CPU_0_REG
       - SYSTEM_CPU_INTEFROM_CPU_1_REG
       - SYSTEM_CPU_INTEFROM_CPU_2_REG
       - SYSTEM_CPU_INTEFROM_CPU_3_REG

5. **17.3.4 Low-power Management Registers**
   - The following registers are used for low-power management.
     For more information, please refer to Chapter 10 Low-power Management (RTC_CNTL):
       - SYSTEM_RTC_FASTMEM_CONFIG_REG: configures the RTC CRC check.

**Footer Information:**
- Page number and document version:
  - "824 ESP32-S3 TRM (Version 1.7)"
- Company name at bottom left corner:
  - Espressif Systems
- Submission link text on right side of footer image placeholder:
  - Submit Documentation Feedback