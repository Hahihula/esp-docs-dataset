**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**Subtitle: Register 2.4. RTC_CNTL_COOPU_CTRL_REG (0x104)**

**Table Description:**  
The table lists various registers and their descriptions related to the ULP coprocessor.

- **Columns**: 
  - Offset
  - Name of register
  - Description
  
| Offset | Name of register | Description |
|--------|------------------|-------------|
| 31     | RTC_CNTL_COOPU_CLKFO | (reserved) |
| ...    | ...              | ...         |
| 0      | RTC_CNTL_COOPU_SHUT_RESET_EN | Reset |

**Register Descriptions:**

- **RTC_CNTL_COCPU_CLKFO**: ULP-RISC-V clock force on. (R/W)
- **RTC_CNTL_COOPU_START_2_RESET_DIS**: Time from ULP-RISC-V startup to pull down reset. (R/W)
- **RTC_CNTL_COOPU_START_2_INTR_EN**: Time from ULP-RISC-V startup to send out RISCV_START_INT interrupt. (R/W)
- **RTC_CNTL_COOPU_SHUT**: Shut down ULP-RISC-V. (R/W)
- **RTC_CNTL_COOPU_SHUT_2_CLK_DIS**: Time from shut down ULP-RISC-V to disable clock. (R/W)
- **RTC_CNTL_COOPU_SHUT_RESET_EN**: This bit is used to reset ULP-RISC-V. (R/W)
- **RTC_CNTL_COOPU_SEL**: select ULP-RISC-V; 1: select ULP-FSM. (R/W)
- **RTC_CNTL_COOPU_DONE FORCE**: O: select ULP-FSM DONE signal; 1: select ULP-RISC-V DONE signal. (R/W)
- **RTC_CNTL_COOPU_DONE**: DONE signal. Write 1 to this bit, ULP-RISC-V will go to HALT and the timer starts counting. (R/W)
- **RTC_CNTL_COOPU_SW_INT_TRIGGER**: Trigger ULP-RISC-V register interrupt. (WO)
- **RTC_CNTL_COOPU_CLKGATE_EN**: Enable ULP-RICS-V clock gate. (WO)

**Section Title: 2.10.2 ULP (RTC_PERI) Registers**

**Body Text:**  
The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter [4 System and Memory](#).

**Footer Information:**  
Espressif Systems  
Page number: **336**  
Document version: ESP32-S3 TRM (Version 1.7)  

**Link Texts**:  
Submit Documentation Feedback