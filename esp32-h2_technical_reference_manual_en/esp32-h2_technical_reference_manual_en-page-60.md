

```markdown
| Name          | Description                                                                                      | Address   | Access |
|---------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| MSIP          | Core local machine software interrupt pending register                                          | 0x1800    | R/W    |
| MTIMECTL      | Core local machine timer interrupt control/status register                                       | 0x1804    | R/W    |
| MTIME         | 64-bit core local timer counter value                                                           | 0x1808    | R/W    |
| MTIMECMP      | 64-bit core local machine timer compare value                                                   | 0x1810    | R/W    |
| USIP          | Core local user software interrupt pending register                                             | 0x1C00    | R/W    |
| UTIMECTL      | Core local user timer interrupt control/status register                                         | 0x1C04    | R/W    |
| UTIME         | Read-only 64-bit core local timer counter value                                                 | 0x1C08    | RO     |
| UTIMECMP      | 64-bit core local user timer compare value                                                      | 0x1C10    | R/W    |
```

## Chapter 1 ESP-RISC-V CPU

### 1.7.4 Timer Counter and Interrupt

The CPU provides a local memory-mapped 64-bit wide M mode timer counter register `MTIME` which has both read/write access. The timer counter can be enabled by setting the `MTCE` bit in `MTIMECTL`.

A read-only memory mapped `UTIME` is also provided for reading the timer counter from U mode, although it always reflects the same value as in the corresponding M mode counter `MTIME` register.

Timer interrupt for M/U mode is enabled by setting the `MTIE/UTIE` bit in `MTIMECTL/UTIMECTL`. Also, the `MTIE/UTIE` bit must be set in `mie` CSR for enabling the interrupt at core level for a particular mode.

Interrupt for M/U mode is asserted when the 64-bit timer value exceeds the 64-bit timer-compare value programmed in `MTIMECMP/UTIMECMP`.

Pending state of M/U mode timer interrupt is reflected as the read-only `MTIP/UTIP` bit in `MTIMECTL/UTIMECTL`.

For de-asserting the pending timer interrupt in M/U mode, either the `MTIE/UTIE` bit has to be cleared or the value of the `MTIMECMP/UTIMECMP` register needs to be updated.

Pending state of this interrupt can be checked at core level for either mode by reading the corresponding bit `MTIP/UTIP` in `mip/uip`.

Upon overflow of the 64-bit timer counter, the `MTOF/UTOF` bit in `MTIMECTL/UTIMECTL` gets set. It can be cleared after appropriate handling of the overflow situation.

Note that by default U mode timer interrupt with ID 4 has the corresponding bit set in `mideleg` CSR. This bit can be toggled for using the interrupt in M mode instead. Similarly the bit corresponding to M mode timer interrupt can be set for using it in U mode.

### 1.7.5 Register Summary

The addresses in this section are relative to CPU sub-system base address provided in Figure 4.2-1 in Chapter 4 System and Memory.

### 1.7.6 Register Description

The addresses in this section are relative to CPU subsystem base address provided in Figure 4.2-1 in Chapter 4 System and Memory.
```