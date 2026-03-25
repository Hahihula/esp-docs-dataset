

# Chapter 15

## Permission Control (PMS)

### 15.1 Overview

The permission control of ESP32-H2 can be divided into two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

The areas managed by PMP and APM are shown in Table 15.1-1.

Table 15.1-1. Management Areas of PMP and AMP

| Slaves/Masters | ROM | HP SRAM | LP SRAM | CPU_PERI¹ | HP_PERI² | LP_PERI³ | EX_MEM⁴ |
|----------------|-----|---------|---------|-----------|----------|----------|---------|
| CPU            | PMP | PMP     | PMP + APM | PMP + APM | PMP + APM | PMP + APM | PMP     |
| Other masters⁵ | N/A | APM     | APM     | N/A       | N/A      | N/A      | N/A     |

---

¹ Peripheral registers in the CPU, address range: 0x600C_0000 – 0x600C_FFFF  
² Peripheral registers in the high-performance system, address range: 0x6000_0000 – 0x600A_FFFF  
³ Peripheral registers in the low-power system, address range: 0x600B_0000 – 0x600B_FFFF  
⁴ External memory, e.g., flash.  
⁵ Masters that can request access to the bus, such as GDMA, MEM_MONITOR. For a complete list of masters, please refer to Table 15.4-1.

Figure 15.1-1. PMP-APM Management Relation

For the CPU, the permission management relation between PMP and APM is shown in Figure 15.1-1. PMP manages the CPU’s access to all address spaces. APM does not manage the CPU’s access to ROM, HP SRAM, and EX_MEM. If the CPU needs to access ROM, HP SRAM, and EX_MEM, it needs permission only from PMP; if it needs to access LP SRAM and other address spaces, it needs to pass PMP’s permission management first and then the APM’s. If the PMP check fails, APM check will not be triggered.