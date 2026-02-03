**Chapter Title:**
Chapter 13 Watchdog Timers (WDT)

**Section Titles and Subsections with Content:**

- **Subsection:** 
  - **Title:** Structure

    - **Diagram Description:**
      The diagram is labeled "Figure 13.3-1. Super Watchdog Controller Structure" which shows the interaction between different components such as Analog, RTC (Real-Time Clock), SWD Controller, and CPU.

- **Subsection:** 
  - **Title:** Workflow

    - **Content Description:**
      In normal state:
        - The S/WD controller receives feed request from S/WD.
        - The S/WD controller can send an interrupt to main CPU or ULP-RISC-V. Main CPU decides whether to feed the SWD directly by setting RTC_CNTL_SWD_FEED, or it sends an interrupt to ULP-RISC-V and asks for feeding through RTC_CNTL_SWD_FEED.
        - When trying to feed S/WD, both CPU and ULP-RISC-V need to disable write protection of S/WD controller. This is done using writing 0x8F1D312A to RTC_CNTL_SWD_WKEY which prevents SWD from being fed by mistake when the system operates in sub-optimal state.
        - If setting RTC_CNTL_SWD_AUTO_FEED_EN to '1', then CPU or ULP-RISC-V can feed S/WD without any interaction with each other.

      After reset:
        - Check RTC_CNTL_RESET_CAUSE PROCPU[5:0] for cause of CPU reset. If RTC_CNTL_RESET_CAUSE PROCPU[5:0] == 0x12, it indicates that the SWD is responsible.
        - Set RTC_CNTL_SWD_RST_FLAG_CLR to clear S/WD reset flag.

- **Subsection:** 
  - **Title:** Interrupts

    - **Content Description:**
      For watchdog timer interrupts refer to Section 12.2.6 Interrupts in Chapter 12 Timer Group (TIMG).

**Footer Information:**

- Page Number:
  - "678"

- Document Title and Version:
  - ESP32-S3 TRM (Version 1.7)

- Company Name:
  - Espressif Systems

- Feedback Link:
  - Submit Documentation Feedback