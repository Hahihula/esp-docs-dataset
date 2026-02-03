**Chapter Title:**
Chapter 15

**Section Titles and Content:**

- **Permission Control (PMS)**
  - *Subsection 15.1 Overview*
    - ESP32-S3 is specially designed for flexible access management to internal memory, external memory, and all peripherals.
    - Once configured, CPU can only access a particular slave device according to the configured permission,
      thus protecting the slave device from unauthorized access (read, write, or instruction execution).
    - In addition, ESP32-S3 has integrated a World Controller which when enabled be used along with Permission Controller
      to allocate the chip’s hardware and software resource into Secure World (World0) and Non-secure World (World1),
      and can switch the CPU between running from the Secure World or Non-secure World.
    - For details, please refer to 16 World Controller (WCL).
    - This chapter mainly describes the access management to different internal memory, external memory
      and peripherals.

  - *Subsection 15.2 Features*
    - ESP32-S3’s Permission Control module supports:
      - Independent access management for the Secure World and Non-secure World.
      - Independent access management to internal memory, including
        - CPU access to internal memory
        - Allocate internal memory as CPU Trace
        - GDMA access to internal memory
      - Independent access management to external memory, including
        - SPI1 access to external memory
        - GDMA access to external memory
        - CACHE access to external memory
      - Independent access management to peripheral regions, including
        - CPU access to peripheral regions
        - Interrupt upon unsupported access alignment
      - Address splitting for more flexible access management
      - Interrupt upon unauthorized access

**Footer:**
Espressif Systems  
683 ESP32-S3 TRM (Version 1.7)  

**Navigation Links and Buttons:**
- GoBack button at the top right corner.
- Submit Documentation Feedback link at the bottom center.

(Note: The text is transcribed as it appears in the image, maintaining structure where possible.)