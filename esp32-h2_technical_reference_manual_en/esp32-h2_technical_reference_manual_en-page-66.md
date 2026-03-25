

# 1.9 Physical Memory Attribute Checker (PMAC)

## 1.9.1 Overview

CPU core also implements a custom Physical Memory Attributes Checker (PMAC) to provide additional permission checks based on pre-defined memory type configured through custom CSRs.

## 1.9.2 Features

PMAC supports below features:

- Configurable memory type for defined memory regions
- Configurable attribute for defined memory regions

## 1.9.3 Functional Description

Software can program the PMAC unit’s configuration and address registers in order to avoid faults due to access to invalid memory regions. PMAC CSRs can only be programmed in machine mode. Once enabled, write, read and execute permission checks are applied to all the accesses irrespective of privilege mode as per programmed values of enabled 16 pma_cfgX and pma_addrX registers (refer to the Register Summary). Access to entries marked as invalid memory types will result in fetch fault or load/store fault exception, as the case may be.

Exception generation and handling for PMAC related faults will be handled in a similar way to PMP checks. When any instruction is being fetched from a memory region configured as null or invalid memory region, an exception is generated at the processor level and the exception cause is set as instruction access fault in mcause CSR. Similarly, any load/store access to null or invalid memory region, will result in an exception generation with mcause updated as load access and store access fault respectively. In case of load/store access faults, violating address is captured in mtval CSR. For the PMAC entries configured as valid memory, the handling is same as for PMP checks.

A lock bit per entry is also provided in case the software wants to disable programming of PMAC registers. Once the lock bit in any pma_cfgX register is set, respective pma_cfgX and pma_addrX registers can not be programmed further, unless a CPU reset cycle is applied.

A 4-bit field in PMAC CSRs is also provided to define attributes for memory regions. These bits are not used internally by CPU core for any purpose. Based on address match, these attributes are provided on load/store interface as side-band signals and are used by cache controller block for its internal operation.