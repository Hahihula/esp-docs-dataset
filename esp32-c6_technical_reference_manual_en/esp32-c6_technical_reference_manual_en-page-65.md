
```markdown
Chapter 1 High-Performance CPU

GoBack

1.8 Physical Memory Protection

1.8.1 Overview

The CPU core includes a Physical Memory Protection (PMP) unit fully compliant to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10, which can be used by software to set memory access privileges (read, write and execute permissions) for required memory regions. In addition to standard PMP checks, CPU core also implements custom Physical Memory Attributes (PMA) checkers to provide additional permission checks based on pre-defined attributes.

1.8.2 Features

The PMP unit can be used to restrict access to physical memory. It supports 16 regions and a minimum granularity of 4 bytes. Maximum supported NAPOT range is 4 GB.

1.8.3 Functional Description

Software can program the PMP unit's configuration and address registers in order to contain faults and support secure execution. PMP CSRs can only be programmed in machine-mode. Once the PMP unit is enabled by configuring PMP CSRs, write, read and execute permission checks are applied to all the accesses in user-mode as per programmed values of enabled 16 pmpcfgX and pmpaddrX registers (refer to the Register Summary).

By default, PMP grants permission to all accesses in machine-mode and revokes permission of all access in user-mode. This implies that it is mandatory to program the address range and valid permissions in pmcfg and pmpaddr registers (refer to the Register Summary) for any valid access to pass through in user-mode.

However, it is not required for machine-mode as PMP permits all accesses to go through by default. In cases where PMP checks are also required in machine-mode, software can set the lock bit of required PMP entry to enable permission checks on it. Once the lock bit is set, it can only be cleared through CPU reset.

When any instruction is being fetched from a memory region without execute permissions, an exception is generated at processor level and exception cause is set as instruction access fault in mcause CSR. Similarly, any load/store access without valid read/write permissions, will result in an exception generation with mcause updated as load access and store access fault respectively. In case of load/store access faults, violating address is captured in mtval CSR.
```