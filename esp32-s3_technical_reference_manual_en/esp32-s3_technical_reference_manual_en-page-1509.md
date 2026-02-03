**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Header:**
GoBack

**Subheader (Register Information):**
- Register 39.62, APB_SARADC_SAR1_PATT_TAB4_REG (0x0024)

**Body Text with Diagrams/Tables:**

1. **Diagram/Table Description for APB_SARADC_SAR1_PATT_TAB4:**
   - Entries are from bits 12 to 15, which correspond to pattern table.
   - Each entry is of length 6-bits (R/W).

2. **Diagram/Table Description for Register 39.63, APB_SARADC_APB_ADC_CTRL_REG:**
   - Bits description:
     - Bit positions from leftmost bit at the top are labeled as follows in descending order.
       - Reserved bits
       - APB_SARADC_ADC_ARB_FIX_PRIORITY (15)
       - APB_SARADC_ADC_ARB_Priority (14-0)

3. **List of Register Entries:**
   - APB_SARADC_ADC_ARC_FORCE, SAR ADC2 arbiter forces to enable RTC ADC2 controller.
     - Access type is R/W
   - APB_SARADC_ADC_WIFI FORCE, SAR ADC2 arbiter forces to enable PWDET controller (R/W)
   - APB_SARADC_ADC_ARC_GRANT FORCE, SAR ADC2 arbiter force grant. (R/W)
   - APB_SARADC_ADC_ARC_RTC_PRIORITY, Set RTC ADC2 controller priority.
     - Access type is R/W
   - APB_SARADC_ADC_ARC_WIFI_PRIORITY, Set PWDET controller priority.

**Footer:**
- Page number 1509
- Document version ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback

**Company Information at the bottom left corner:** 
Espressif Systems