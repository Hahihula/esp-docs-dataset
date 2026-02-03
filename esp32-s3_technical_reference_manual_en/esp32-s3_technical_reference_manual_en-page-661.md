**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Table of Contents with Descriptions and Access Information**

- **Name:** TIMG_RTCCALICFG_REG  
  **Description:** RTC frequency calculation configuration register 0  
  **Address:** 0x0068  
  **Access:** varies

- **Name:** TIMG_RTCCALICFG1_REG  
  **Description:** RTC frequency calculation configuration register 1  
  **Address:** 0x006C  
  **Access:** RO (Read Only)

- **Name:** TIMG_RTCCALICFG2_REG  
  **Description:** RTC frequency calculation calibration register 2  
  **Address:** 0x0080  
  **Access:** varies

**Interrupt registers**

- **Name:** TIMG_INT_ENA_TIMERS_REG  
  **Description:** Interrupt enable bits  
  **Address:** 0x0070  
  **Access:** R/W (Read/Write)

- **Name:** TIMG_INT_RAW_TIMERS_REG  
  **Description:** Raw interrupt status  
  **Address:** 0x0074  
  **Access:** R/WTC/SS

- **Name:** TIMG_INT_ST_TIMERS_REG  
  **Description:** Masked interrupt status  
  **Address:** 0x0078  
  **Access:** RO (Read Only)

- **Name:** TIMG_INT_CLR_TIMERS_REG  
  **Description:** Interrupt clear bits  
  **Address:** 0x007C  
  **Access:** WT

**Version register**

- **Name:** TIMG_NTIMERS_DATE_REG  
  **Description:** Timer version control register  
  **Address:** 0x00F8  
  **Access:** R/W (Read/Write)

**Timer group configuration registers**

- **Name:** TIMG_REGCLK_REG  
  **Description:** Timer group clock gate register  
  **Address:** 0x00FC  
  **Access:** R/W (Read/Write)

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)