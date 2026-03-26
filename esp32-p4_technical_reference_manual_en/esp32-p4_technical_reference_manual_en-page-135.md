

```markdown
Chapter 1 High-Performance CPU

GoBack

1.10 Memory Protection Unit

Each HP core implements standard RISC-V physical memory protection (PMP) scheme along with custom physical memory attribute checker (PMAC) logic to prevent unauthorized memory access.

1.10.1 Standard Physical Memory Protection

1.10.1.1 Overview

The CPU core includes a physical memory protection (PMP) unit, which is fully compliant with RISC-V Instruction Set Manual, Volume I: Privileged Architecture, Version 1.10. It can be used by software to set memory access privileges (read, write and execute permissions) for required memory regions. In addition to standard PMP checks, the CPU core also implements custom physical memory attributes (PMA) checkers to provide additional permission checks based on pre-defined attributes.

1.10.1.2 Features

The PMP unit can be used to restrict access to physical memory. The main features are:

* Up to 32 PMP entries
* Minimum address granularity of 128 bytes
* Three address matching modes: OFF, TOR (Top of Range), and NAPOT (Naturally Aligned Power-of-Two). NA4 (Naturally Aligned 4-Byte Region) address matching mode is not supported
* Permission controls for read, write, and execute
* Lock function for each PMP entry
* Maximum physical space address of 4 GB

1.10.1.3 Functional Description

Software can program the PMP unit’s configuration and address registers in order to contain faults and support secure execution. PMP CSRs can only be programmed in machine mode. Once the PMP unit is enabled by configuring PMP CSRs, write, read and execute permission checks are applied to all the accesses in user mode as per programmed values of the enabled 16 pmcpgx and pmpaddrx registers (refer to Section 1.10.1.4).

By default, PMP grants permission to all accesses in machine mode and revokes permission of all access in user mode. This implies that it is mandatory to program the address range and valid permissions in pmcfg and pmpaddr registers (refer to Section 1.10.1.4) for any valid access to pass through in user mode. However, it is not required for machine mode as PMP permits all accesses to go through by default. In cases where PMP checks are also required in machine mode, software can set the lock bit of required PMP entry to enable permission checks on it. Once the lock bit is set, it can only be cleared through CPU reset.

When any instruction is being fetched from a memory region without execute permissions, an exception is generated at processor level and exception cause is set as instruction access fault in mcause CSR. Similarly, any load/store access without valid read/write permissions will result in an exception generation with mcause updated as load access and store access fault respectively. In case of load/store access faults, violating address is captured in mtval CSR.

Espressif Systems
135
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```