

```markdown
| LP_APMO_REG | LP_APMO_CTRL | 1 | LP_APMO_FUNC_CTRL_REG | 4 | LP_APMO_REGION_FILTER_EN_REG |
| LP_APM_REG   | LP_APM_CTRL  | 2 | LP_APM_FUNC_CTRL_REG | 4 | LP_APM_REGION_FILTER_EN_REG |

### 16.3.2.2 Address Ranges

* HP_APM_REG register module can configure up to 16 groups of address ranges for functional module HP_APM_CTRL. The start and end address for each region (address range) can be configured by setting `HP_APM_REGIONn_ADDR_START` and `HP_APM_REGIONn_ADDR_END` respectively. Configure the bit `n` of `HP_APM_REGION_FILTER_EN_REG` to enable region `n`. The first group of address ranges is enabled by default.
* LP_APMO_REG register module can configure up to 4 groups of address ranges for functional module LP_APMO_CTRL. The start and end address for each region can be configured by setting `LP_APMO_REGIONn_ADDR_START` and `LP_APMO_REGIONn_ADDR_END`. Configure the bit `n` of `LP_APMO_REGION_FILTER_EN_REG` to enable region `n`. The first group of address ranges is enabled by default.
* LP_APM_REG register module can configure up to 4 groups of address ranges for functional module LP_APM_CTRL. The start and end address for region `n` can be configured by setting `LP_APM_REGIONn_ADDR_START` and `LP_APM_REGIONn_ADDR_END`. Configure the bit `n` of `LP_APM_REGION_FILTER_EN_REG` to enable region `n`. The first group of address ranges is enabled by default.

When configuring the address ranges, the address requires 4-byte alignment (the lower two bits of the address are 0). For example, the address range could be set as `0x4080000C ~ 0x40808774` or `0x600C0008 ~ 0x600CFF70`.

### 16.3.2.3 Access Permissions of Address Ranges

Within each address range, access permissions (read/write/execute) can be configured for different security modes:

* The master in TEE mode always has read, write, and execute permissions in the address range.
* For master in REE0, REE1 or REE2 mode, access permissions can be configured in `HP_APM_REGIONn_ATTR_REG`, `LP_APM_REGIONn_ATTR_REG` or `LP_APMO_REGIONn_ATTR_REG` based on the access path.

Different access paths managed by the same register module share the configuration of address ranges and access permissions. For example, the permission management of data path HP_APM MO-M3 shown in figure 16.3-1 should follow the address ranges and access permissions of each address range configured in the register module `HP_APM_REG`. Likewise, the permission management of data path LP_APM MO-M1 shown in figure 16.3-1 should follow the address ranges and access permissions of each address range configured in the register module `LP_APM_REG`.

For the access path HP_APM M1, all masters except HP CPU and LP CPU access HP_MEM through this data access path. Suppose that `HP_APM_M1_FUNC_EN` is enabled and a master in REE1 mode needs to access HP_MEM through HP_APM M1. The whole process is as follows:
```