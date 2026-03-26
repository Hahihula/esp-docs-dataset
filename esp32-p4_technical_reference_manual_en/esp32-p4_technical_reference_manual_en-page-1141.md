

```markdown
Chapter 19 Permission Control (PMS)
GoBack

## 19.2 Features

The APM module has the following features:

* Up to 32 configurable address ranges for each DMA master
* Access permission management for each CPU core to access internal memory, external memory, and peripheral registers
* Support for interrupts
* Support for exception information record

## 19.3 Functional Description

### 19.3.1 Architecture

The APM module contains three parts and five register modules as follows:

* **DMA APM**, containing register group `HP_DMA_PMS_REG`, responsible for:
    - configuring up to 32 address regions for DMA masters
    - managing the access permission to each address region for each DMA master

* **HP APM**, containing register groups `HP_PERI_PMS_REG` and `LP2HP_PERI_PMS_REG`, responsible for managing the access permissions to peripheral registers (HP CPU PERI, HP PERI), internal memory (HP ROM, HP L2MEM), and external memory (EXT MEM) in the HP system, specifically,
    - managing the access permissions for HP CPUO/1 in user mode to access all the above-mentioned slaves
    - managing the access permissions for HP CPUO/1 in machine mode to access all the above-mentioned slaves
    - managing the access permissions for LP CPU in machine mode to access all the above-mentioned slaves

* **LP APM**, containing register groups `LP_PERI_PMS_REG` and `HP2LP_PERI_PMS_REG`, responsible for managing the access permissions to peripheral registers (LP PERI) and internal memory (LP SRAM) in the LP system, specifically,
    - managing the access permissions for HP CPUO/1 in user mode to access LP PERI and LP SRAM
    - managing the access permissions for HP CPUO/1 in machine mode to access LP PERI and LP SRAM
    - managing the access permissions for LP CPU in machine mode to access LP PERI

Figure 19.3-1 shows the access paths managed by APM and the corresponding register groups.
```