

```markdown
Chapter 1 Bus Architecture  
GoBack

- **GDMA bus**: Provides two connections, one to the bus matrix, the other to the external memories. It is used by the GDMA to perform transfers, including peripheral-to-memory, memory-to-peripheral, peripheral-to-peripheral, and memory-to-memory operations. Targets include HP SRAM, LP SRAM, and external memories. When accessing external memory, it is recommended to use a longer burst length whenever possible to ensure data throughput.
- **SDIO SLAVE bus**: Connects the SDIO SLAVE to the bus matrix. It is used to access data in peripherals or memories. Targets include HP SRAM, LP SRAM, HP&LP peripherals and CPU peripherals.

Note:
Accessing LP SRAM via TRACE, TCM MEM MONITOR, or PSRAM MEM MONITOR is not recommended, because these paths are slow, and LP SRAM has limited space.
```