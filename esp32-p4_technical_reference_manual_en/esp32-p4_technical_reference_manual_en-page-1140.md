

```markdown
1 DMA masters that support DMA transfers, such as VDMA, USB 2.0 OTG, MEM_MONITOR, etc.
2
• HP ROM (0x4FC0_0000 - 0x4FC1_FFFF)
• HP L2MEM (0x4FF0_0000 - 0x4FFB_FFFF)
• EXT MEM, including external flash (0x4000_0000 - 0x43FF_FFFF) and external RAM (0x4800_0000 - 0x4BFF_FFFF)
3 "Direct access" means HP CPU0/1 accesses internal and external memory mapped into the following address spaces without going through the cache:
• HP ROM (0x8FC0_0000 - 0x8FC1_FFFF)
• HP L2MEM (0x8FF0_0000 - 0x8FFB_FFFF)
• EXT MEM, including external flash (0x8000_0000 - 0x83FF_FFFF) and external RAM (0x8800_0000 - 0x8BFF_FFFF)
4 HP CPU peripheral registers (0x3FF0_0000 - 0x3FF1_FFFF)
5 HP system peripheral registers (0x5000_0000 - 0x500F_FFFF)
6 LP system peripheral registers (0x5011_0000 - 0x5012_FFFF)
7 As can be seen from the table, APM includes HP APM, LP APM, and DMA APM, which will be described in the following sections.

Figure 19.1-1. PMP-APM Management Relation

The diagram illustrates that when the HP CPUs access HP ROM, HP SPM, HP L2MEM, and EXT MEM, the access paths are solely managed by PMP. On the other hand, when the HP CPUs access the peripheral registers, HP ROM, HP L2MEM, and EXT MEM without going through the cache, the access paths are controlled by both PMP and APM. If the PMP check fails, the APM permission control will not be triggered.

PMP-related registers are located inside the HP CPUs and can be read or configured with special instructions. For how to configure PMP, please refer to Chapter 1 High-Performance CPU > 1.10.1 Standard Physical Memory Protection.

The following sections will provide a detailed introduction to the features, functions, and configurations of the APM module. When referring to HP CPU0/1, accessing HP ROM/HP L2MEM/EXT MEM always means direct access to HP ROM/HP L2MEM/EXT MEM.
```