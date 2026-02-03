**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Heading:**
16.5 World Switch Log

**Body Text:**
In actual use cases, CPU is switching between two worlds quite frequently and has to deal with nested interrupts. To be able to restore to the previous world, World Controller keeps a world switching log in a series of registers, which is called “World Switch Log Table”.

**Subsection Heading:**
16.5.1 Structure of World Switch Log Register

**Body Text:**
ESP32-S3’s World Switch Log Table consists of 13 WCL_CORE_m_STATUSTABLEn_REG(n: 1-13) registers (see Figure 16.5-1). The world switching address configured in WCL_CORE_m_ENTRY_x_ADDR_REG, which is monitored at Entry x, is logged in WCL_CORE_m_STATUSTABLEx_REG.

**Table Description:**
StatusTable
| current | from_entry | from_world |
|---------|------------|------------|
| 5       | 4          | 1          |
|         |            | 0          |

**Figure Caption and Description:**
Figure 16.5-1. World Switch Log Register

- WCL_CORE_m_FROM_WORLD_n: logs the world information before the world switch.
  - 0: CPU was in Secure World
  - 1: CPU was in Non-secure World
  
- WCL_CORE_m_FROM ENTRY_n: logs the entry information before the world switch.
  - 0: CPU was not at any interrupts monitored at any entry.
  - 1 – 13: CPU was at the interrupt monitored at a certain entry.

- WCL_CORE_m_CURRENTn: indicates if CPU is at the interrupt monitored at the current entry. When CPU is at the interrupt monitored at Entry x,
  - WCL_CORE_m_CURRENT_x is updated to 1, and the same fields of all other entries are updated to 0.

**Subsection Heading:**
16.5.2 How World Switch Log Registers Are Updated

**Body Text:**
To explain this process, assuming:

1. At the beginning:
   - CPU is running in the Non-secure World;
   - Registers WCL_CORE_m_STATUSTABLEn_REG(n: 1-13) are all empty.

2. Then an interrupt occurs at Entry 9;

3. Then another interrupt with higher priority occurs at Entry 1;

4. Then the last interrupt with highest priority occurs at Entry 4.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32-S3 TRM (Version 1.7)
Page number not visible in image