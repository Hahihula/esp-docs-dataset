

```markdown
1. HP_APM M1 will first determine whether the address requested to access is within the 16 address ranges configured in the `HP_APM_REG` register module. If 16 groups of address ranges are partially enabled, HP_APM M1 will only determine whether the address requested to access is within the enabled address ranges.
2. Assuming that the address requested to access is within second group of configured address ranges, then determine whether the address range of this group is enabled, that is, whether bit 1 of `HP_APM_REGION_FILTER_EN` is 1.
3. If the address range is enabled, judge whether the master has read permission for the second group of address ranges in REE1 mode, that is, whether `HP_APM_REGION1_R1_R` in `HP_APM_REGION1_ATTR_REG` is valid (that is, 1). If valid, the read request will be allowed. Otherwise it will return 0.

When the HP power domain (see chapter Low-Power Management) powered down and restarted, the LP CPU does not have access to HP_MEM by default. The master must be in the TEE mode to configure `LP_TEE_FORCE_ACC_HPMEM_EN` in the LP power domain. When `LP_TEE_FORCE_ACC_HPMEM_EN` is enabled, the LP CPU can access the HP_MEM without the permission management of APM controller.

The address ranges configured above may overlap. For example, region 1 and region 2 overlap. If region 1 is set to be unreadable and region 2 is set to be readable, in this case the overlapping area of region 1 and region 2 is readable. The same rules apply for write and execute permissions.

Note:
* When powered up, only the HP CPU is in TEE mode by default, and the other masters are in REE2 mode. By default, APM controller blocks access requests from all master in REEO, REE1, and REE2 modes.
* All registers listed in 16.6 Register Summary can only be configured by the master in TEE security mode.

## 16.4 Programming Procedure

* Configure the HP CPU to machine mode (ie. TEE mode).
* Choose the security mode of the master by configuring `TEE_Mn_MODE` or `LP_TEE_Mn_MODE`. `n` here equals to the master ID in Table 18.4-5.
* Configure the start and end address for access address ranges by setting
    * `HP_APM_REGIONn_ADDR_START`, `HP_APM_REGIONn_ADDR_END`, or
    * `LP_APMO_REGIONn_ADDR_START`, `LP_APMO_REGIONn_ADDR_END`, or
    * `LP_APM_REGIONn_ADDR_START`, `LP_APM_REGIONn_ADDR_END`.
* Configure the access permissions of each region in different security mode by configuring
    * `HP_APM_REGIONn_ATTR_REG` or `LP_APM_REGIONn_ATTR_REG` or `LP_APMO_REGIONn_ATTR_REG`.
* Set the bit `n` of `HP_APM_REGION_FILTER_EN_REG` or `LP_APM_REGION_FILTER_EN_REG` or `LP_APMO_REGION_FILTER_EN_REG` to enable region `n`.
* Configure `HP_APM_FUNC_CTRL_REG`, `LP_APM_FUNC_CTRL_REG` or `LP_APMO_FUNC_CTRL_REG` enable permission management of different access paths (enabled by default).

Take I2S accessing HP_MEM via GDMA as an example, assuming that it is only allowed to read and write in the fourth group address range 0x40805000 ~ 0x4080F000 address range:
```