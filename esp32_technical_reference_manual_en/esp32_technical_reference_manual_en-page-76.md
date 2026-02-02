**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Section Titles with Page Numbers:**
- GoBack

**Subsection Heading:**
4.3.2 MPU/MMU

**Body Text for Subsection "4.3.2 MPU/MMU":**
The MPU and MMU manage on-chip memories, off-chip memories, and peripherals. To do this they are based on the process of accessing the peripheral or memory region. More specifically, when a code tries to access a MMU/MPU-protected memory region or peripheral, the MMU or MPU will receive the PID from the PID generator that is associated with the CPU on which the process is running.

For on-chip memory and peripherals, the decisions the MMU and MPU make are only based on this PID, whereas the specific CPU the code is running on is not taken into account. Subsequently, the MMU/MPU configuration for the internal memory and peripherals allows entries only for the eight different PIDs. In contrast, the MMU moderating access to the external memory takes not only the PID into account, but also the CPU the request is coming from. This means that MMUs have configuration options for every PID when running on the APP_CPU, as well as every PID when running on the PRO_CPU. While, in practice, accesses from both CPUs will be configured to have the same result for a specific process, doing so is not a hardware requirement.

The decision an MPU can make, based on this information, is to allow or deny a process to access the memory region or peripheral. An MMU has the same function, but additionally it redirects the virtual memory access, which the process acquired into physical memory that possibly reach out an entirely different physical memory regions. This way, MMU-governed memory can be remapped on a process-by-process basis.

**Subsection Heading:**
4.3.2.1 Embedded Memory

**Body Text for Subsection "4.3.2.1 Embedded Memory":**
The on-chip memory is governed by fixed-function MPUs, configurable MPUs, and MMUs:

**Table Title with Table Number in italics:**
*Table 4.3-1. MPU and MMU Structure for Internal Memory*

| Name       | Size   | Address range         | Governed by        |
|------------|--------|-----------------------|--------------------|
| ROM0      | 384 KB | From 0x4000_0000 To    | Static MPU        |
|            |        |                       |                    |
| ROM1      | 64 KB  | From 0x3FF9_0000 To   | Static MPU        |
|            |        |                       |                    |
| SRAMO     | 128 KB | From 0x4007_0000 To   | Static MPU        |
|            |        |                       |                    |
| RAM1 (aliases) | 128 KB | From 0x3FFE_0000 To    | Static MPU        |
|            |        |                       |                    |
| SRAM1     | 72 KB  | From 0x400A_0000 To   | Static MPU        |
|            |        |                       |                    |
| RAM2      | 8 KB   | From 0x3FFB_E000 To   | Static MPU        |
|            |        |                       |                    |
| RTC FAST (aliases) | 8 KB    | From 0x400C_0000 To   | RTC FAST MPU      |
|            |        |                       |                    |
| RTC SLOW (aliases) | 8 KB     | From 0x5000_0000 To   | RTC SLOW MPU      |

**Body Text for Subsection "4.3.2.1 Embedded Memory":**
Static MPUs

ROMO, ROM1, the lower 64 KB of SRAMO, SRAM1 and the lower 72 KB of SRAM2 are governed by a static MPU. The behaviour of these MPUs is hardwired and cannot be configured by software. They moderate access to the memory region solely through the PID of the current process. When the PID of the process is O

**Footer:**
Espressif Systems
76 ESP32 TRM (Version 5.6)
Submit Documentation Feedback