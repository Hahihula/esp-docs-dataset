Title: Chapter 15 Permission Control (PMS)

Subtitle: 15.4.1 Access Configuration

Body Text:
ESP32-S3’s CPU can be configured with different read (R) and write (W) accesses to most of its modules and peripherals independently, from the Secure World and the Non-secure World, by configuring respective registers (`PMS_CORE_m_PIF_PMS_CONSTRAN_n_REG`).

Note that permission to modules and peripherals can be configured independently for CPU0 and CPU1 and for the Secure World and Non-secure World.

Notes on `PMS_CORE_m_PIF_PMS_CONSTRAN_n_REG`:
- m can be 0 or 1 for CPU0 and CPU1 respectively.
- n can be 1~8, in which 1~4 are for Secure World and 5~8 are for Non-secure World.

For example, users can configure `PMS_CORE_0_PIF_PMS CONSTRAINT_1_REG [1:0]` to 0x2, meaning CPU0 is granted with read access but not write access from the Secure World to UART0. In this case, CPU0 won’t be able to modify the UART0’s internal registers when in Secure World.

Table Title:
Table 15.4-1. Access Configuration of the Peripherals

Column Headers: 
- Peripherals
- Secure World (with sub-columns PIF_PMS_CONSTRAN_4_REG and PIF_PMS_CONSTRAN_8_REG)
- Non-secure World (with sub-columns PIF_PMS_CONSTRAN_8_REG [Bit 3])
- Bit Range

Content Summary:
The table lists various peripherals along with their corresponding register configurations in the Secure World, specifically `PIF_PMS_CONSTRAN_4_REG` and `PIF_PMS_CONSTRAN_8_REG`, as well as bit ranges for non-secure world access.

Footer: 
Espressif Systems
Page number 694 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

(Note: The actual content of the table is not fully transcribed due to its length, but it follows a similar structure as described above.)