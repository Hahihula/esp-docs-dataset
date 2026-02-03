**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Diagram Title and Description:**
Figure 10.6-1. ESP32-S3 Boot Flow

**Flowchart Steps in Diagram:**

1. **Wake up**
   - Static Vector Sel:
     - If "Running in ROM":
       - `reset_vector@0x40000400`
         - Initialization
           - Calc CRC in fast RTC mem (Yes)
             - Jump to entry point in RTC fast mem, Running in RTC fast mem.
               - Return?
                 - Yes: Run code in CPU RAM; No: SPI Boot -> Run code in CPU RAM

     - If "Running in ROM":
       - `reset_vector@0x50000000`
         - Initialization
           - Calc CRC in slow RTC mem (No)
             - Run code in RTC slow mem, Running in RTC slow mem.
               - Return?
                 - Yes: Run code in CPU RAM; No:

**Footer Information:**
Espressif Systems  
583 ESP32-S3 TRM (Version 1.7)  

**Link Texts at the Bottom of Page:** 
Submit Documentation Feedback

**Navigation Link on Top Right Corner:**
GoBack