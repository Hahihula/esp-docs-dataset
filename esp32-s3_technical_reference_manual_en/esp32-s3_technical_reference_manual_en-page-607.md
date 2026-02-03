**Title: Chapter 10 Low-power Management (RTC_CNTL)**

**Subheading: Register 10.25. RTC_CNTL_RTC_CLK_CONF_REG (0x0074)**

**Binary Table Representation of the Register Bits**
- The table shows a binary representation with labels for each bit position, ranging from bits 31 to 0.

**Description and Functionality List**

1. **RTC_CNTL_EFUSE_CLK FORCE_GATING**
   - Set this bit to force eFuse gating.
   - Access: Read/Write

2. **RTC_CNTL_EFUSE_CLK FORCE_NOGATING**
   - Set this bit to force no eFuse gating.

3. **RTC_CNTL_CK8M_DIV SEL_VLD**
   - Synchronizes the reg_ck8m_div_sel, not that you have to invalidate the bus before switching clock and validate new clock.
   - Access: Read/Write

4. **RTC_CNTL_CK8M_DIV**
   - Set the CK8M_D256_OUT divider:
     - 00: divided by 128
     - 01: divided by 256 (10)
     - 11: divided by 512

5. **RTC_CNTL_ENB_CK8M**
   - Set this bit to disable CK8M and CK8M_D256_OUT.
   - Access: Read/Write

6. **RTC_CNTL_ENB_CK8M_DIV**
   - Selects the CK8M_D256_OUT:
     - 1: CK8M
     - 0: CK8M divided by 256.

7. **RTC_CNTL_DIG_XTAL32K_EN**
   - Set this bit to enable CK_XTAL_32K clock for the digital core.
   - Access: Read/Write

8. **RTC_CNTL_DIG_CLK8M_DIV_EN**
   - Set this bit to enable CK8M_D256_OUT clock for the digital core.

9. **RTC_CNTL_DIG_CLK8M_EN**
   - Set this bit to enable 8 MHz clock for the digital core.
   - Access: Read/Write

10. **RTC_CNTL_CK8M_DIV SEL**
    - Stores the 8 MHz divider, which is reg_ck8m_div_sel + 1.

11. **RTC_CNTL_XTAL FORCE_NOGATING**
    - Set this bit to force no gating during sleep.
    - Access: Read/Write

12. **RTC_CNTL_CK8MFORCE_NOGATING**
    - Set this bit to disable force gating for the 8 MHz crystal during sleep.

**Footer Note:** Continued on the next page...

**Company Information and Document Details**

- Company Name: Espressif Systems
- Page Number: 607
- Document Title: ESP32-S3 TRM (Version 1.7)
- Links: Submit Documentation Feedback