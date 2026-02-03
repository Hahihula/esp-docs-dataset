**Chapter Title:**
Chapter 7 Reset and Clock

**GoBack Link:** (Located at the top right corner)

**List of Points under Chapter Heading:**
- Core Reset: resets the whole digital system except RTC, including CPU0, CPU1, peripherals, Wi-Fi, Bluetooth® LE (BLE), and digital GPIOs.
- System Reset: resets the whole digital system, including RTC.
- Chip Reset: resets the whole chip.

**Bullet Point List under Chapter Heading:**
- Support software reset and hardware reset:
  - Software reset is triggered by CPU configuring its corresponding registers.
  - Hardware reset is directly triggered by the circuit.

**Note Box (Highlighted):**
If CPU Reset is from CPU0, the PMS registers will be reset, too.

**Subsection Title with Number:**
7.1.4 Functional Description

**Body Text under Subsection Heading:**
CPUO and CPU1 will be reset immediately when any of the reset above occurs. After the reset is released, CPUO and CPU1 can read from the registers RTC_CNTL_RESET_CAUSE_PROCPU and RTC_CNTL_RESET_CAUSE_APPCPU to get the reset source, respectively. The reset sources recorded in the two registers are shared by the two CPUs, except the CPU reset sources, i.e., each CPU has its own CPU reset sources.

**Reference Table:**
Table 7-1 lists the reset sources and the types of reset they trigger.

**Footer Information (Left-aligned):**
Espressif Systems

**Page Number:** 
527

**Document Version Note at Bottom Right Corner:**
ESP32-S3 TRM (Version 1.7)

**Link for Submitting Documentation Feedback:**
Submit Documentation Feedback