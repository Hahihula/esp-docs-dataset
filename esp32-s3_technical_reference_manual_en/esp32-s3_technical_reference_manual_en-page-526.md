**Chapter Title:**
Chapter 7

**Section Titles and Content:**

- **Reset and Clock**

    - **Subsection (7.1 Reset):**
        - **Overview:** ESP32-S3 provides four reset levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset.
        
            All reset levels mentioned above (except Chip Reset) maintain the data stored in internal memory.

- **Architectural Overview:**

    Figure 7.1-1 shows an architectural overview of ESP32-S3 with labeled components such as:
    
        - CPU0
        - CPU1
        - Wi-Fi
        - Bluetooth LE
        - System Reset
        - Chip Reset

- **Subsection (7.1.2 Architectural Overview):**
    Figure 7.1-1 is referenced again for clarity.

- **Features:**

    Support four reset levels:
    
    - CPU Reset only resets the CPU core.
    - CPUx can be CPU0 or CPU1 here.
    - Once such a reset occurs, programs will execute from CPUx reset vector.
    - Each CPU core has its own reset logic. 

**Footer Information:** 
- Page number: 526
- Document title: ESP32-S3 TRM (Version 1.7)
- Company name and logo: Espressif Systems

**Navigation Link:**
- GoBack button at the top right corner of the page.

**Figure Caption for Figure 7.1-1:** Reset Levels