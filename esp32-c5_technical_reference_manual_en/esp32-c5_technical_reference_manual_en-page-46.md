

```markdown
Chapter 1 Bus Architecture
```

## Chapter 1

### Bus Architecture

The ESP32-C5 SoC employs a multi-layer bus matrix as the core of its communication architecture, interconnecting multiple masters and slaves through an efficient structure. This architecture supports concurrent access, effectively mitigating conflicts so that the high-performance and low-power RISC-V cores, DMA controllers, debug interfaces, and various peripherals can operate simultaneously with minimal contention. By optimizing data flow and system performance, the bus matrix ensures efficient system operation even when multiple high-speed peripherals are running at the same time.

The main system of the ESP32-C5 SoC consists of:

- Nine masters:
  - High-performance (HP) 32-bit RISC-V processor I-bus, D-bus, and AHB bus
  - Low-power (LP) 32-bit RISC-V processor
  - TRACE
  - TCM MEM MONITOR
  - PSRAM MEM MONITOR
  - GDMA
  - SDIO SLAVE

- Six slaves:
  - ROM
  - HP SRAM
  - LP SRAM
  - Cache
  - HP&LP peripherals
  - CPU peripherals

The bus architecture of the SoC is shown below.
```