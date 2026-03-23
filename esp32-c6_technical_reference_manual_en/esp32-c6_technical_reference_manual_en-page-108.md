

```markdown
- 32-bit AHB system bus for peripheral and memory access
- Core performance metric events
- Able to wake up the HP CPU and send an interrupt to it
- Access to HP memory and LP memory
- Access to the entire peripheral address space


## 3.2 Configuration and Status Registers (CSRs)

### 3.2.1 Register Summary

Below is a list of CSRs available to the CPU. Except for the custom performance counter CSRs, all the implemented CSRs follow the standard mapping of bit fields as described in the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. It must be noted that even among the standard CSRs, not all bit fields have been implemented, limited by the subset of features implemented in the CPU. Refer to the next section for a detailed description of the subset of fields implemented under each of these CSRs.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Machine Information CSR** |  |  |  |
| mhartid | Machine Hart ID | 0xF14 | RO |
| **Machine Trap Setup CSRs** |  |  |  |
| mstatus | Machine Mode Status | 0x300 | R/W |
| misa¹ | Machine ISA | 0x301 | R/W |
| mie | Machine Interrupt Enable | 0x304 | R/W |
| mtvec² | Machine Trap Vector | 0x305 | R/W |
| **Machine Trap Handling CSRs** |  |  |  |
| mscratch | Machine Scratch | 0x340 | R/W |
| mepc | Machine Trap Program Counter | 0x341 | R/W |
| mcause³ | Machine Trap Cause | 0x342 | R/W |
| mtval | Machine Trap Value | 0x343 | R/W |
| mip | Machine Interrupt Pending | 0x344 | R/W |
| **Trigger Module CSRs (shared with Debug Mode)** |  |  |  |
| tselect | Trigger Select Register | 0x7A0 | R/W |
| tdata1 | Trigger Abstract Data 1 | 0x7A1 | R/W |
| tdata2 | Trigger Abstract Data 2 | 0x7A2 | R/W |
| **Debug Mode CSRs** |  |  |  |
| dcsr | Debug Control and Status | 0x7B0 | R/W |
| dpc | Debug PC | 0x7B1 | R/W |
| dscratch0 | Debug Scratch Register 0 | 0x7B2 | R/W |
| dscratch1 | Debug Scratch Register 1 | 0x7B3 | R/W |
| **Machine Counter/Timer CSRs** |  |  |  |

¹Although misa is specified as having both read and write access (R/W), its fields are hardwired and thus write has no effect. This is what would be termed WARL (Write Any Read Legal) in RISC-V terminology.
²mtvec only provides configuration for trap handling in vectored mode with the base address aligned to 256 bytes.
³External interrupt IDs reflected in mcause include even those IDs which have been reserved by RISC-V standard for core internal sources.
```