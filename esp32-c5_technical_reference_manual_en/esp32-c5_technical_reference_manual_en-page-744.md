

```markdown
CPU_APM_CTRL. The start and end addresses of each region are configured by
CPU_APM_REGIONn_ADDR_START and CPU_APM_REGIONn_ADDR_END. Configure the bit n of
CPU_APM_REGION_FILTER_EN_REG to enable region n. Region 0 (i.e., the first address range) is enabled by default.

When configuring the address ranges, the address requires a 4-byte alignment (the lower two bits of the address are 0). For example, the address range could be set to 0x4080000C ~ 0x40808774 or 0x600C0008 ~ 0x600CFF70.

18.5.2.2.2 Access Permissions of Address Ranges

For each address range, the access permissions (read/write/execute) are configurable in different security modes:

*   Masters in TEE mode always have read, write, and execute permissions in the address range.
*   For masters in REE0, REE1 or REE2 mode, access permissions can be configured with HP_APM_REGIONn_ATTR_REG, LP_APM_REGIONn_ATTR_REG, or LP_PMO_REGIONn_ATTR_REG based on the access path.

Different access paths managed by the same register module share the configuration of address ranges and access permissions. For example, the permission management of data paths HP_APM_CTRL MO-M4 shown in Figure 18.5-1 should follow the address ranges and access permissions of the 16 address ranges configured in the register module HP_APM_REG. Likewise, the permission management of data path LP_APM_CTRL MO-M1 shown in Figure 18.5-1 should follow the address ranges and access permissions of the four address ranges configured in the register module LP_APM_REG.

Take HP SRAM as an example. All masters access it through HP_APM_CTRL M1, except that the HP CPU accesses it through PMP and CPU_APM_CTRL, and the LP CPU accesses it through HP_APM M2. Suppose that HP_APM_M1_FUNC_EN is enabled and a master in REE1 mode needs to access HP SRAM. The whole process is as follows:

1.  HP_APM_CTRL M1 will first determine whether the address requested to access is within the 16 address ranges configured in the HP_APM_REG register module.
2.  Assuming that the address requested to access is within the second address range, then HP_APM_CTRL M1 determines whether the address range is enabled, that is, whether bit 1 of HP_APM_REGION_FILTER_EN is 1.
3.  If the address range is enabled, HP_APM_CTRL M1 checks whether the master has read permission for the second address range, that is, whether HP_APM_REGION1_R1_R in HP_APM_REGION1_ATTR_REG is 1. If valid, the read request will be allowed, otherwise, 0 will be returned.

When the HP power domain (please refer to Chapter 13 Low-Power Management) restarts after power-down, the LP CPU does not have access to HP SRAM by default. In TEE mode, you can configure LP_TEE_FORCE_ACC_HPMEM_EN to 1 for the LP CPU to access HP SRAM without requiring permission checks from the SYS_APM controller.

Note:

*   When the chip is powered up, only the HP CPU is in TEE mode by default, and other masters are in REE2 mode. By default, the SYS_APM controller blocks access requests from all masters in REE0, REE1, and REE2 modes.
```