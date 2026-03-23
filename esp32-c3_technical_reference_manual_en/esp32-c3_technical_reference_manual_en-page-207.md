

```markdown
## 8.3.2 CPU Interrupts

The ESP32-C3 implements its interrupt mechanism using an interrupt controller instead of RISC-V Privileged ISA specification. The ESP-RISC-V CPU has 31 interrupts, numbered from 1 ~ 31. Each CPU interrupt has the following properties.

- Priority levels from 1 (lowest) to 15 (highest).
- Configurable as level-triggered or edge-triggered.
- Lower-priority interrupts mask-able by setting interrupt threshold.

**Note:**
For detailed information about how to configure CPU interrupts, see Chapter 1 ESP-RISC-V CPU.

## 8.3.3 Allocate Peripheral Interrupt Source to CPU Interrupt

In this section, the following terms are used to describe the operation of the interrupt matrix.

- `Source_X`: stands for a peripheral interrupt source, wherein X means the number of this interrupt source in Table 8.3-1.
- `INTERRUPT_COREO_SOURCE_X_MAP_REG`: stands for a configuration register for the peripheral interrupt source (`Source_X`).
- `Num_P`: the index of CPU interrupts, can be 1 ~ 31.
- `Interrupt_P`: stands for the CPU interrupt numbered as Num_P.

### 8.3.3.1 Allocate one peripheral interrupt source (Source_X) to CPU

Setting the corresponding configuration register `INTERRUPT_COREO_SOURCE_X_MAP_REG` of Source_X to Num_P allocates this interrupt source to Interrupt_P.

### 8.3.3.2 Allocate multiple peripheral interrupt sources (Source_Xn) to CPU

Setting the corresponding configuration register `INTERRUPT_COREO_SOURCE_Xn_MAP_REG` of each interrupt source to the same Num_P allocates multiple sources to the same Interrupt_P. Any of these sources can trigger CPU Interrupt_P. When an interrupt signal is generated, CPU should check the interrupt status registers to figure out which peripheral generated the interrupt. For more information, see Chapter 1 ESP-RISC-V CPU.

### 8.3.3.3 Disable CPU peripheral interrupt source (Source_X)

Clearing the configuration register `INTERRUPT_COREO_SOURCE_X_MAP_REG` disables the corresponding interrupt source.

## 8.3.4 Query Current Interrupt Status of Peripheral Interrupt Source

Users can query current interrupt status of a peripheral interrupt source by reading the bit value in `INTERRUPT_COREO`
```