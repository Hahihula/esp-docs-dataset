

```markdown
Chapter 1 High-Performance CPU

GoBack

1.10.2 Custom Physical Memory Attribute (PMA) Checker

1.10.2.1 Overview

CPU core also implements a custom physical memory attributes checker (PMAC) to provide additional permission checks based on pre-defined memory types configured through custom CSRs. Please note that the PMA checks are applied irrespective of the core’s privilege mode, i.e., it doesn’t differentiate between machine and user mode.

1.10.2.2 Features

PMAC supports below features:

* 16 PMA entries
* Configurable memory type for defined memory regions
* Minimum address granularity of 128 bytes
* Three address matching mode: OFF, TOR (Top of Range) and NAPOT (Naturally Aligned Power-of-Two). NA4 (Naturally Aligned 4-Byte Region) address matching mode is not supported
* Permission controls for read, write and execute
* Lock function for each PMA entry
* Maximum physical space address of 4 GB
* Configurable attribute for defined memory regions

1.10.2.3 Functional Description

Software can program the PMAC unit’s configuration and address registers in order to avoid faults due to access to invalid memory regions. PMAC CSRs can only be programmed in machine mode. Once enabled, write, read and execute permission checks are applied to all the accesses irrespective of privilege mode as per programmed values of enabled 16 pma_cfgX and pma_addrX registers (refer to Section 1.10.2.4). Access to entries marked as invalid memory types will result in fetch fault or load/store fault exception, as the case may be.

Exception generation and handling for PMAC related faults will be handled in similar way to PMP checks. When any instruction is being fetched from a memory region configured as a null or an invalid memory region, an exception is generated at the processor level and the exception cause is set as instruction access fault in mcause CSR. Similarly, any load/store access to a null or an invalid memory region will result in an exception generation with mcause updated as load access or store access fault respectively. In case of load/store access faults, violating address is captured in mtval CSR. For the PMAC entries configured as valid memory, the handling is same as for PMP checks.

A lock bit per entry is also provided in case software wants to disable programming of PMAC registers. Once the lock bit in any pma_cfgX register is set, respective pma_cfgX and pma_addrX registers can not be programmed further, unless a CPU reset cycle is applied.

A 4-bit field in PMAC CSRs is also provided to define attributes for memory regions. These bits are not used internally by the CPU core for any purpose. Based on address match, these attributes are provided on
```