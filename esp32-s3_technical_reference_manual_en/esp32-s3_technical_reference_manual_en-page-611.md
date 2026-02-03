**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
Register 10.30. RTC_CNTL_DIG_PWC_REG (0x090)

**Table Description:**
- The table lists various register bits related to power control in the digital system.
- Columns include bit names and their corresponding values.

**Bit Definitions with Descriptions:**

- **RTC_CNTL_LSLP_MEM FORCE_PD**: Set this bit to FPD the memories in the digital system in sleep. (R/W)
  
- **RTC_CNTL_LSLP_MEM FORCE PU**: Set this bit to FPU the memories in the digital system. (R/W)

- **RTC_CNTL_DG PERI FORCE_PD**: Set this bit to FPD PDU peripherals. (R/W)

- **RTC_CNTL_DG PERI FORCE PU**: Set this bit to FPU PDU peripherals. (R/W)

- **RTC_CNTL_WIFI FORCE_PD**: Set this bit to FPD Wi-Fi. (R/W)

- **RTC_CNTL_WIFI FORCE PU**: Set this bit to FPU Wi-Fi. (R/W)

- **RTC_CNTL_DG PERI FORCE_PD**: Set this bit to FPD the digital core. (R/W)

- **RTC_CNTL_DG WRAP FORCE_PD**: Set this bit to FPD the CPU in sleep.

- **RTC_CNTL_CPU TOP FORCE_PD**: Set this bit to FPD the CPU and Wi-Fi circuit in sleep. (R/W)

- **RTC_CNTL_CPU TOP FORCE PU**: Set this bit to FPU the CPU, PD peripherals in sleep. (R/W)

- **RTC_CNTL_DG PERI PD EN**: Set this bit to enable PDU for the digital system.

- **RTC_CNTL_CPU TOP PD EN**: Set this bit to enable PDU for the CPU and Wi-Fi circuit in sleep.
  
- **RTC_CNTL_WIFI PD EN**: Set this bit to enable PDU for the Wi-Fi circuit. (R/W)

- **RTC_CNTL_DG WRAP PD EN**: Set this bit to enable FPD.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback