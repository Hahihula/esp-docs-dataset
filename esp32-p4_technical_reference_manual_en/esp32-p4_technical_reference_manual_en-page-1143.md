

```markdown
- Fixed address ranges
  - The fixed address ranges are the valid address spaces of peripheral registers, internal memory, and external memory. See the table notes under Table 19.1-1 for the address ranges of internal and external memory. Refer to Chapter 7 System and Memory > Table 7.3-2 for the address ranges of each peripheral.
    - To manage access to the fixed address ranges, please refer to Figure 19.3-1 for the access paths and their corresponding register groups.
- Configurable Address Range
  - APM can configure eight address ranges with PMS_PERI_REGIONn/m_LOW_REG and PMS_PERI_REGIONn/m_HIGH_REG (n/m = 0 ~ 7) in LP_PERI_PMS_REG. These configurable address ranges can be used by HP CPUs and LP CPU to access all on-chip peripheral registers (HP CPU PERI, HP PERI, LP PERI).
    - The access permissions are managed by PMS_PERI_REGION_PMS_REG in LP_PERI_PMS_REG.
When managing access permissions to peripheral registers, the permission management for the configurable address range should precede that of the fixed address range. Specifically:
  - If the access address is within the configurable address range, then APM will check if this access is permitted to access the configurable address range.
    - If permitted, APM will continue to check if the access is permitted to the fixed address range.
    - If not permitted, the access will be denied and skip the permission check to the fixed address range.
  - If the access address is outside the configurable address range, then it will skip the configurable address range check, but will continue to the fixed address range check.
- The management of configurable address ranges is a supplement to the management of fixed address ranges. For example, users can configure access permissions for a fixed address range, and deny access to two configurable ranges within the fixed range, resulting in a fixed address range containing two access-disabled address ranges.

19.3.2.2 Address Ranges Managed by DMA APM

The register group HP_DMA_PMS_REG provides 32 sets of registers (PMS_DMA_REGIONn_LOW_REG ~ PMS_DMA_REGIONn_HIGH_REG, n = 0 ~ 31) to configure address ranges for DMA masters to access. Note that since the address must be aligned to 4K bytes, the lowest 12 bits are set to 0.
HP_DMA_PMS_REG provides separate read and write permissions for each DMA master to access each address range.

19.4 Programming Procedure

As HP CPUs can work in either user mode or machine mode, HP APM and LP APM grant specific access permissions for each work mode. Therefore, users need to configure the work mode for HP CPUs first in order for the HP CPUs to access internal memory, external memory, and peripheral registers.
```