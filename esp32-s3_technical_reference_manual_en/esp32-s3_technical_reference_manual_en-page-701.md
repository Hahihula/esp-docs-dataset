**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Table Titles and Content:**

1. **Table 15.6-4. Interrupt Registers for Unauthorized Access to Internal Memory via GDMA**
   - **Registers Table:**
     - PMS_DMA_APBPERI_PMS_MONITOR_1_REG
       - Bit [0]: Clears interrupt signal (Description)
       - Bit [1]: Enables interrupt (Description)
     - PMS_DMA_APBPERI_PMS_MONITOR_2_REG
       - Bit [0]: Stores interrupt signal (Description: Stores the world the CPU was in when the unauthorized access happened. 0b01: Secure World; 0b10: Non-secure World) 
       - Bit [2:43]: Stores the address that GDMA was trying to access unauthorized
     - PMS_DMA_APBPERI_PMS_MONITOR_3_REG
       - Bit [0]: Stores the access direction. 1: write; 0: read (Description)
       - Bit [16:1]: Stores the byte information of unauthorized access

2. **Table 15.6-5. Interrupt Registers for Unauthorized PIF Access**
   - **Registers Table:**
     - PMS_CORE_m_PIF_PMS_MONITOR_1_REG
       - Bit [0]: Clears interrupt signal and logged information (Description)
       - Bit [7:6]: PIF access happened 0b01: Secure World; 0b10: Non-secure World 
       - Bit [5]: Stores the access direction. 1: write; 0: read
     - PMS_CORE_m_PIF_PMS_MONITOR_2_REG
       - Bit [4:2]: Stores the data type of unauthorized access (Description)
       - Bit [1]: Stores the access type. 0: instruction; 1: data 
     - PMS_CORE_m_PIF_PMS_MONITOR_3_REG
       - Bit [31:0]: Stores the address of unauthorized access

**Section Title and Content:**
- **Section Heading:** 15.6.5 Interrupt upon Unauthorized Peripheral Bus (PIF) Access
- **Body Text:**
  ESP32-S3 can be configured to trigger interrupts when PIF attempts to access RTC FAST memory, RTC SLOW memory, and peripheral regions without configured permission, and log the information about this unauthorized access. Note that once this interrupt is enabled, it's enabled for all RTC FAST memory, RTC SLOW memory, and peripheral regions, and cannot only be enabled for a certain address field. This interrupt corresponds to the CORE_m_PIF_PMS_MONITOR_VIOLATE_INR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback