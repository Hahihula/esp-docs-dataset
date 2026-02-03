**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Table Header:**
- Name
- Description
- Address
- Access

**Row in Table:**
- RTC_I2C_DATE_REG
- Version control register
- Ox00FC
- R/W

**Section Title: 2.10 Registers**

**Subsection Title: 2.10.1 ULP (ALWAYS_ON) Registers**

**Body Text:**
The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Figure Caption:** Register 2.1. RTC_CNTL_ULP_CP_TIMER_REG (0x00FC)

**Register Description with Binary Layouts:**

- **RTC_CNTL_ULP_CP_PC_INIT**
  - ULP coprocessor PC initial address.
  - Access: R/W

- **RTC_CNTL_ULP_CP_GPIO_WAKEUP_ENA**
  - Enable the option of ULP timer woken up by RTC GPIO.

- **RTC_CNTL_ULP_CP_GPIO_WAKEUP_CLR**
  - Disable the option of ULP timer woken up by RTC GPIO.
  - Access: WO

- **RTC_CNTL_ULP_CP_SLT_TIMER_EN**
  - ULP coprocessor timer enable bit. 
  - Description:
    - Enable hardware timer.

**Figure Caption:** Register 2.2. RTC_CNTL_ULP_CP_TIMER_1_REG (0x0134)

**Register Description with Binary Layouts:**

- **RTC_CNTL_ULP_CP_TIMER_SLP_CYCLE**
  - Set sleep cycles for ULP coprocessor timer.
  - Access: R/W

**Footer Information:** 
Espressif Systems
Page number: 334
Document version and title: ESP32-S3 TRM (Version 1.7)
Link to submit feedback or documentation information is provided at the bottom of the page.

(Note: The binary layout for each register includes bits numbered from rightmost bit as '0' up to leftmost bit.)