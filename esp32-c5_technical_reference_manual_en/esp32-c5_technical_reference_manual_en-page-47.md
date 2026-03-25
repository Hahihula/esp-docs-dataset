

```markdown
Note:

1. The circles at the intersections in the figure indicate that the bus in the corresponding column can access the slave in the corresponding row.
2. The GDMA has a data path that bypasses the bus matrix and directly accesses the external memory.
3. When the CPU accesses external memory, it must go through the cache. In most cases, the cache is transparent to the user.

Figure 1.0-1. ESP32-C5 Bus Architecture

Below is the description of each bus shown in Figure 1.0-1 ESP32-C5 Bus Architecture:

*   **HP CPU I-bus**: Connects the instruction bus of the high-performance (HP) 32-bit RISC-V processor to the bus matrix. It is used by the core to fetch instructions. Targets include ROM, HP SRAM, and external memory through MSPI.
*   **HP CPU D-bus**: Connects the data bus of the high-performance (HP) 32-bit RISC-V processor to the bus matrix. It is used by the core for literal load and debug access. Targets include ROM, HP SRAM, and external memory through MSPI.
*   **HP CPU AHB bus**: Connects the AHB bus of the high-performance (HP) 32-bit RISC-V processor to the bus matrix. It is used to access data located in a peripheral or in LP SRAM. Targets include LP SRAM, HP&LP peripherals and CPU peripherals.
*   **LP CPU bus**: Connects the AHB bus of the low-power (LP) 32-bit RISC-V processor to the bus matrix. It is used by LP CPU to access memories and peripherals. Targets include HP SRAM, LP SRAM and HP&LP peripherals.
*   **TRACE bus**: Connects the TRACE to the bus matrix. It is used for certain debugging operations. Targets include HP SRAM and LP SRAM.
*   **TCM MEM MONITOR bus**: Connects the TCM MEM MONITOR to the bus matrix. It is used to write the monitoring information recorded by the TCM MEM MONITOR into the memory. Targets include HP SRAM and LP SRAM.
*   **PSRAM MEM MONITOR bus**: Connects the PSRAM MEM MONITOR to the bus matrix. It is used to write the monitoring data from the PSRAM MEM MONITOR into the memory. Targets include HP SRAM and LP SRAM.
```