**Chapter Title:**
Chapter 7 Reset and Clock

**Table Header:**
Table 7-1- PRO_CPU and APP_CPU Reset Reason Values

| PRO    | APP   | Source                   | Reset Type     | Note                                    |
|--------|-------|--------------------------|----------------|-----------------------------------------|
| 0x01   | 0x01  | Chip Power On Reset     | System Reset   | -                                       |
| 0x10   | 0x10  | RWDT System Reset        | System Reset   | See WDT Chapter                        |
| 0x0F   | 0x0F  | Brown Out Reset         | System Reset   | See Power Management Chapter            |
| 0x03   | 0x03  | Software System Reset    | Core Reset     | Configure RTC_CNTRL_SW_SYS_RST register.|
| 0x05   | 0x05  | Deep Sleep Reset        | Core Reset     | See Power Management Chapter            |
| 0x06   | 0x06  | SDIO Reset               | Core Reset     | Reserved                                |
| 0x07   | 0x07  | MWDTO Global Reset      | Core Reset     | See WDT Chapter                        |
| 0x08   | 0x08  | MWDTO1 Global Reset     | Core Reset     | See WDT Chapter                        |
| 0x09   | 0x09  | RWDT Core Reset         | Core Reset     | See WDT Chapter                        |
| 0xB    | -     | MWDTO CPU Reset          | CPU Reset      | See WDT Chapter                        |
| 0xC    | -     | Software CPU Reset       | CPU Reset      | Configure RTC_CNTRL_SW_APPCPU_RST register.|
| 0x1B   | -     | MWDTT1 CPU Reset        | CPU Reset      | See WDT Chapter                        |
| 0x0C   | 0x0D  | Software CPU Reset       | CPU Reset      | Configure RTC_CNTRL_SW_APPCPU_RST register.|
| 0x0D   | RWDT  | RWDT CPU Reset          | CPU Reset      | See WDT Chapter                        |
| -      | OxE   | PRO CPU Reset           | CPU Reset      | Indicates that the PRO CPU has independently reset the APP CPU by configuring the DPOR_APPCPU_RESETTING register.|

**Section Title:**
7.2 System Clock

**Subsection 1:**
7.2.1 Introduction
The ESP32 integrates multiple clock sources for the CPU cores, the peripherals and the RTC. These clocks can be configured to meet different requirements. Figure 7.2-1 shows the system clock structure.

**Footer Information:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback