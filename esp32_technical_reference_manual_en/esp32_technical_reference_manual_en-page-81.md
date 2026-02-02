**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Title:**
Table 4.3-7. DPORT_DMMU_TABLEn_REG & DPORT_IMMU_TABLEn_REG

| [6:4] Access rights for PID 2 ~ 7 | [3:0] Address authority |
|----------------------------------|-------------------------|
| O                                 | Virtual page 0 accesses this physical page. |
| 1                                 | All of PIDs 2 ~ 7 have access.             |
| 2                                 | Only PID 2 has access.                     |
| 3                                 | Only PID 3 has access.                     |
| 4                                 | Only PID 4 has access.                     |
| 5                                 | Only PID 5 has access.                     |
| 6                                 | Only PID 6 has access.                     |
| 7                                 | Only PID 7 has access.                     |

**Subsection Title:**
Differences Between SRAMO and SRAM2 MMU

**Body Text for Subsection on Differences Between SRAMO and SRAM2 MMU:**

The memory governed by the SRAMO MMU is accessed through the processors I-bus, while the processor accesses the memory governed by the SRAM2 MMU through the D-bus. Thus, the normal envisioned use is for the code to be stored in the SRAMO MMU pages and data in the MMU pages of SRAM2. In general, applications running under a PID of 2 to 7 are not expected to modify their own code, because for these PIDs access to the MMU pages of SRAM is read-only. These applications must, however, be able to modify their data section, so that they are allowed to read as well and write MMU pages located in SRAM2. As stated before, processes running under PID 0 or 1 always have full read-and-write access to both memory ranges.

**Subsection Title:**
DMA MPU

**Body Text for Subsection on DMA MPU:**

Applications may want to configure the DMA to send data straight from or to the peripherals they can control. With access to DMA, a malicious process may also be able to copy data from or to a region it cannot normally access. In order to be secure against that scenario, there is a DMA MPU which can be used to disallow DMA transfers from memory regions with sensitive data in them.

For each 8 KB region in the SRAM1 and SRAM2 regions, there is a bit in the DPORT_AHB_MPU_TABLEn_REG registers which tells the MPU to either allow or disallow DMA access to this region. The DMA MPU uses only these bits to decide if a DMA transfer can be started; the PID of the process is not a factor. This means that when the OS wants to restrict its processes in a heterogeneous fashion, it will need to re-load these registers with the values applicable to the process to be run on every context switch.

The register bits that govern access to the 8 KB regions are detailed in Table 4.3-8. When a register bit is set, DMA can read/write the corresponding 8 KB memory range. When the bit is cleared, access to that memory range is denied.

**Footer:**
Espressif Systems
Page Number: 81

**Document Version Information:** 
ESP32 TRM (Version 5.6)

**Navigation Links:**
- GoBack