**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Register Information:**
- **Register Name:** RTC_CNTL_DIG_ISO_REG (0x094)
- **Description of Register Bits and Values**

| Bit Number | Description                                      |
|------------|---------------------------------------------------|
| 31         | RTC_CNTL_DG_WRAPE FORCE_NOISO                     |
| 30         | RTC_CNTL_WIFC TOP FORCE_NOISO                      |
| ...        | ...                                               |
| 2          | RTC_CNTL_CPU_TOP FORCE_NOISO                       |
| 1          | RTC_CNTL_WIFI_FORCE_ISO                            |
| 0          | RTC_CNTL_WIWI FORCE_NOISO                          |

**Bit Descriptions:**

- **RTC_CNTL_DG_PAD_AUTOHOLD (RO)**
  - Indicates the auto-hold status of the digital GPIOs.

- **RTC_CNTL_CLR_DG_PAD_AUTOHOLD (WO)**
  - Ste this bit to clear the auto-hold enabler for the digital GPIOs. (R/W)

- **RTC_CNTL_DG_PAD_AUTOHOLD_EN (RW)**
  - Set this bit to allow the digital GPIOs to enter the autohold status.

- **RTC_CNTL_DG_PAD FORCE_NOISO (RW)**
  - Set this bit to disable the force isolation to the digital GPIOs. (R/W)

- **RTC_CNTL_DG_PAD FORCE_ISO (RW)**
  - Set this bit to force isolate the digital GPIOs.
  
- **RTC_CNTL_DG_PAD FORCE_UNHOLD (RW)**
  - Set this bit for the force hold unhold the digital GPIOs.

- **RTC_CNTL_DG_PAD FORCE_HOLD (RW)**
  - Set this bit as the force isolation of the digital GPIOs. (R/W)

- **RTC_CNTL_DG_PERI_FORCE_NOISO (RW)**
  - Set this bit to disable the force isolation for the digital peripherals.
  
- **RTC_CNTL_CPU_TOP FORCE_ISO (RW)**
  - Set this bit to isolate from the CPU.

- **RTC_CNTL_WIFI_FORCE_ISO (RW)**
  - Set this bit as a force hold unhold of Wi-Fi circuits. 

- **RTC_CNTL_WIWI FORCE_NOISO (RW)**
  - Set this bit for disable isolation on Wi-Fi circuits.
  
- **RTC_CNTL_DG_WRAPE FORCE_ISO (RW)**
  - Set this bit to isolate the digital system.

- **RTC_CNTL_DG_WRAPE FORCE_NOISO (RW)**
  - Set this bit as a force hold unhold of Digital System. 

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)

**GoBack Link:** [Link to previous page or section]