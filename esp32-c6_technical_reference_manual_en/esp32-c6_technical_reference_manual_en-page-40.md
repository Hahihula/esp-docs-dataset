

```markdown
- Branch target buffer (BTB) with static branch prediction
- User (U) mode support along with interrupt delegation
- Interrupt controller with up to 28 external vectored interrupts for both M and U modes with 16 programmable priority and threshold levels
- Core local interrupts (CLINT) dedicated for each privilege mode
- Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Support for instruction trace
- Debugger with a direct system bus access (SBA) to memory and peripherals
- Hardware trigger compliant to the specification RISC-V External Debug Support Version 0.13 with up to 4 breakpoints/watchpoints
- Physical memory protection (PMP) and attributes (PMA) for up to 16 configurable regions
- 32-bit AHB system bus for peripheral access
- Configurable events for core performance metrics

## 1.3 Terminology

branch an instruction which conditionally changes the execution flow  
delta a change in the program counter that is other than the difference between two instructions placed consecutively in memory  
hart a RISC-V hardware thread  
retire the final stage of executing an instruction, when the machine state is updated  
trap the transfer of control to a trap handler caused by either an exception or an interrupt

## 1.4 Address Map

Below table shows address map of various regions accessible by CPU for instruction, data, system bus peripheral and debug.

Table 1.4-1. CPU Address Map

| Name       | Description             | Starting Address | Ending Address   | Access |
|------------|-------------------------|------------------|------------------|--------|
| IRAM/DRAM  | Instruction/Data region | 0x4000_0000      | 0x4FFF_FFFF      | R/W    |
| CPU        | CPU Sub-system region   | 0x2000_0000      | 0x2FFF_FFFF      | R/W    |
| AHB        | AHB Peripheral region   | *default         | *default         | R/W    |

*default: Address not matching any of the specified ranges (IRAM, DRAM, CPU) are accessed using AHB bus.
```