

```markdown
- Operating clock frequency of up to 40 MHz
- 18 vector interrupts
- Debug module compliant with RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Hardware trigger compliant with RISC-V External Debug Support Version 0.13 with up to 2 breakpoints/watchpoints
- Core performance metric events
- Wake-up interrupt for HP CPU
- Access to HP memory and LP memory
- Access to the entire peripheral address space

## 3.3 Configuration and Status Registers (CSRs)

### 3.3.1 Register Summary

Below is a list of CSRs that are supported by the LP CPU. Except for the custom performance counter CSRs, all the implemented CSRs follow the standard mapping of bit fields as described in the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. It must be noted that even among the standard CSRs, not all bit fields have been implemented, limited by the subset of features implemented in the CPU. For a detailed description of the subset of fields implemented under each of these CSRs, please refer to Section 3.3.2.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```