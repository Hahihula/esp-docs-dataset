

```markdown
Chapter 16 Permission Control (PMS)

Different access paths managed by the same register module share the configuration of address ranges and access permissions. For example, the permission management of data paths HP_APM_CTRL MO-M3 follows the address ranges and access permissions of the 16 address ranges configured in the HP_APM_REG register module. Likewise, the permission management of data path LP_APM_CTRL MO follows the address ranges and access permissions of the four address ranges configured in the LP_APM_REG register module. The permission management of data paths CPU_APM_CTRL MO-M1 follows the address ranges and access permissions of the eight address ranges configured in the CPU_APM_REG register module.

For HP SRAM, all masters access it through HP_APM_CTRL M1, except that the HP CPU accesses it through PMP and CPU_APM_CTRL. Suppose that HP_APM_M1_FUNC_EN is enabled and a master in REE1 mode needs to access HP SRAM. The whole process is as follows:

1.  HP_APM_CTRL M1 first determines whether the address requested to access is within the 16 address ranges configured in the HP_APM_REG register module.
2.  Assuming that the address requested to access is within the second address range, then HP_APM_CTRL M1 determines whether the address range is enabled, that is, whether bit 1 of HP_APM_REGION_FILTER_EN is 1.
3.  If the address range is enabled, HP_APM_CTRL M1 checks whether the master has read permission for the second address range, that is, whether HP_APM_REGION1_R1_R in HP_APM_REGION1_ATTR_REG is 1. If valid, the read request will be allowed, otherwise, 0 will be returned.

Note:

*   When the chip is powered up, only the HP CPU is in TEE mode by default, and other masters are in REE2 mode. By default, the APM controller blocks access requests from all masters in REEO, REE1, and REE2 modes.
*   All registers listed in 16.8 Register Summary can only be configured by the masters that are in TEE security mode.
*   The configured address ranges may overlap. For example, if one region is set to be unreadable and another region readable, then the overlapping area of the two regions is readable. The same rules apply to write and execute permissions.
*   Configure HP_APM_REGIONn_LOCK and LP_APM_REGIONn_LOCK to lock the configuration of the start and end address of REGIONn and its access permission. Only chip reset, system reset, and core reset can unlock the configurations and restore all configurations in APM registers to their default values.

16.6 Programming Procedure

For a master to access memory or peripheral registers, follow the programming procedures below:

1.  Set the HP CPU to the machine mode (i.e., TEE mode).
2.  Configure TEE_Mn_MODE to choose the security mode of the master. The master ID n is defined in Table 16.5-1.
3.  Configure HP_APM_REGIONn_ADDR_START and HP_APM_REGIONn_ADDR_END, LP_APM_REGIONn_ADDR_START and LP_APM_REGIONn_ADDR_END, or CPU_APM_REGIONn_ADDR_START and CPU_APM_REGIONn_ADDR_END to define the start and end address of the access address ranges.
```