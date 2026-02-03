**Chapter Title:**
Chapter 16 World Controller (WCL)

**GoBack Link:** GoBack

**Section Header:**
Register 16.16 WCL_CORE_0_NMI_MASK_TRIGGER_ADDR_REG (0x0184)

**Field Description and Values:**
- **Field Name:** WCL_CORE_0_NMI_MASKTriggerAddr
- **Description:** Configures the address at which the NMI masking stops for CPUO.
  - **Access Type:** Read/Write ((R/W))
  - **Reset Value:** 31

**Section Header:**
Register 16.17 WCL_CORE_0_NMI_MASK_DISABLE_REG (0x0188)

**Field Description and Values:**
- **Field Name:** WCL CORE_0 NMI MaskDisable
- **Description:** Write any value to this field so CPUO checks NMI masking.
  - **Access Type:** Write Only ((WO))
  - **Reset Value:** 31

**Section Header:**
Register 16.18 WCL_CORE_0_NMI_MASK_CANCEL_REG (0x018C)

**Field Description and Values:**
- **Field Name:** WCL CORE_0 NMI MaskCancel
- **Description:** Write any value to this field to cancel CPUO’s NMI masking.
  - **Access Type:** Write Only ((WO))
  - **Reset Value:** 31

**Footer Information:**
Espressif Systems  
820 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback