**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Section Header:**
Register 9.34. RTC_CNTL_SW_CPU_STALL_REG (0x00AC)

**Diagram Description for Register 9.34:**
- The diagram shows a bit map with labels such as "RTC_CNTL_SWSTALL_PROCPU_C1" and "RTC_CNTL_SWSTALL_APPCPU_C1".
- Bits are numbered from right to left, starting at '0' on the far-right side.

**Register Description (9.34):**
- **Field Name:** RTC_CNTL_SW_STALL_PROCPU_C1
  - **Description:** `reg_rtc_cntl_sw_stall_procpu_c1[5:0]`
  - **Value Explanation:** 
    - `reg_rtc_cntl_sw_stall_procpu_c0[1:0] == 0x86 (100001 10)` will stall PRO_CPU.
    - See also RTC_CNTL_OPTIONSO_REG for more details.

- **Field Name:** RTC_CNTL_SWSTALL_APPCPU_C1
  - **Description:** `reg_rtc_cntl_sw_stall_appcpu_c1[5:0]`
  - **Value Explanation:** 
    - `reg_rtc_cntl_sw_stall_appcpu_c0[1:0] == 0x86 (100001 10)` will stall APP_CPU.
    - See also RTC_CNTL_OPTIONSO_REG for more details.

**Section Header:**
Register 9.35. RTC_CNTL_STOREn_REG

**Diagram Description for Register 9.35:**
- The diagram shows a bit map with labels such as "RTC_CNTL STOREn" and numbered bits from '0' to '31'.

**Register Description (9.35):**
- **Field Name:** RTC_CNTL_STOREn
  - **Description:** `32-bit general-purpose retention register`
  - **Access Mode:** Read/Write

**Footer:**
Espressif Systems  
Page Number: 219  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback