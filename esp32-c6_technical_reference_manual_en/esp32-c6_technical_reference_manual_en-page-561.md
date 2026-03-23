

# Chapter 16

## Permission Control (PMS)

### 16.1 Overview

The permission management of ESP32-C6 can be divided into two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

The areas managed by PMP and APM are shown in the table 16.1-1. The first column lists the masters and the first row lists the slaves. For the CPU, the permission management relation between PMP and APM is shown in Figure 16.1-1.

For example, to access the ROM, the master HP CPU needs the permission from PMP; and to access the LP_MEM, the master HP CPU needs permission from PMP and APM. It is worth noting that HP CPU passes the PMP permission management first and then the APM. If the PMP check fails, the APM permission management will not be triggered.

For HP CPU, PMP manages the access permission of all address spaces, but APM can't manage HP CPU's access to HP_MEM and ROM.

Table 16.1-1. Management Area of PMP and APM

| | ROM | HP_MEM | LP_MEM | CPU_PERI¹ | HP_PERI² | LP_PERI³ |
|---|---|---|---|---|---|---|
| HP CPU | PMP | PMP | PMP + APM | PMP + APM | PMP + APM | PMP + APM |
| LP CPU | N/A | APM | APM | N/A | APM | APM |
| SDIO slave | N/A | APM | APM | APM | APM | APM |
| Others⁴ | N/A | APM | APM | N/A | N/A | N/A |

¹ Peripheral registers in the HP CPU, address range: 0x600C_0000 – 0x600C_FFFF  
² Peripheral registers in the high-performance system, address range: 0x6000_0000 – 0x600A_FFFF  
³ Peripheral registers in the low-power system, address range: 0x600B_0000 – 0x600B_FFFF  
⁴ Masters that can request access to the bus, such as GDMA, MEM_MONITOR. For a complete list of masters, please refer to Table 18.4-5.