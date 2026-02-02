**Chapter Title:**
Chapter 7

**Section Titles and Subtitles:**
- Reset and Clock
- System Reset (Subtitle)
- Introduction (Subsection)

**Body Text:**
The ESP32 has three reset levels: CPU reset, Core reset, and System reset. None of these reset levels clear the RAM.

**Figure Caption:** 
Figure 7.1-1 shows the subsystems included in each reset level.
- **Diagram Description**: The diagram is labeled "System" with various components such as RTC, PMU, Sensor, ULP, and DIG GPIO on one side; CPU (with Wi-Fi), Core, Bluetooth, PERI are shown within a box. 

**List:**
- CPU reset: Only resets the registers of one or both of the CPU cores.
- Core reset: Resets all the digital registers, including CPU cores, external GPIO and digital GPIO. The RTC is not reset.
- System reset: Resets all the registers on the chip, including those of the RTC.

**Subsection Title:** 
7.1.2 Reset Source

**Body Text for Subsection 7.1.2:**
While most of the time the APP_CPU and PRO_CPU will be reset simultaneously, some reset sources are able to reset only one of the two cores. The reset reason for each core can be looked up individually:

- `PRO_CPU` reset reason is stored in `RTC_CNTL_RESET_CAUSE_PROCPU`
- `APP_CPU` reset reason is found using `RTC_CNTL_RESET_CAUSE_APPCPU`

**Table Reference:**
Table 7.1-1 shows the possible reset reason values that can be read from these registers.

**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number**:  
165