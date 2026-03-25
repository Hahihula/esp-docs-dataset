

```markdown
15.4.2.2 Address Ranges

HP_APM_REG register module can configure up to 16 address ranges for functional module HP_APM_CTRL.
The start and end address for each region (address range) are configured by HP_APM_REGIONn_ADDR_START
and HP_APM_REGIONn_ADDR_END, respectively. Configure the bit n of HP_APM_REGION_FILTER_EN_REG
to enable the (n+1)th region. The first address range is enabled by default.

LP_APM_REG register module can configure up to four address ranges for functional module LP_APM_CTRL.
The start and end address for each region are configured by LP_APM_REGIONn_ADDR_START and
LP_APM_REGIONn_ADDR_END. Configure the bit n of LP_APM_REGION_FILTER_EN_REG to enable the
(n+1)th region. The first address range is enabled by default.

When configuring the address ranges, the address requires 4-byte alignment (the lower two bits of the
address are 0). For example, the address range could be set as 0x4080000C ~ 0x40808774 or 0x600C0008
~ 0x600CFF70.

15.4.2.3 Access Permissions of Address Ranges

For each address range, the access permissions (read/write/execute) can be configured for different security
modes:

* The master in TEE mode always has read, write, and execute permissions in the address range.
* For master in REEO, REE1 or REE2 mode, access permissions can be configured in
  HP_APM_REGIONn_ATTR_REG or LP_APM_REGIONn_ATTR_REG based on the access path.

Different access paths managed by the same register module share the configuration of address ranges and
access permissions. For example, the permission management of data path HP_APM_CTRL MO-M3 shown in
Figure 15.4-1 should follow the address ranges and access permissions of each address range configured in
the register module HP_APM_REG. Likewise, the permission management of data path LP_APM_CTRL MO
shown in Figure 15.4-1 should follow the address ranges and access permissions of each address range
configured in the register module LP_APM_REG.

As Figure 15.4-1 shows, all masters access HP_MEM through the HP_APM_CTRL M1 path. Suppose that
HP_APM_M1_FUNC_EN is enabled and a master in REE1 mode needs to access LP_MEM. The whole process
is as follows:

1. HP_APM_CTRL M1 will first determine whether the address requested to access is within the 16 address
ranges configured in the HP_APM_REG register module.

2. Assuming that the address requested to access is within the second address range, then
HP_APM_CTRL M1 determines whether the address range is enabled, that is, whether bit 1 of
HP_APM_REGION_FILTER_EN is 1.

3. If the address range is enabled, HP_APM_CTRL M1 checks whether the master has read permission for
the second address range, that is, whether HP_APM_REGION1_R1_R in HP_APM_REGION1_ATTR_REG is
valid (that is, 1). If valid, the read request will be allowed, otherwise 0 will be returned.

The address ranges configured may overlap. For example, region 1 and region 2 overlap. If region 1 is set to be
unreadable and region 2 readable, then the overlapping area of region 1 and region 2 is readable. The same
rules apply for write and execute permissions.
```