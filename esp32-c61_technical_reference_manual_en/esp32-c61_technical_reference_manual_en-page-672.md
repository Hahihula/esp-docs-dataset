

```markdown
| APM Controllers | Register Modules | Number of Access Paths | Enable Permission Management | Number of Configurable Address Ranges | Enable Address Ranges |
|-----------------|------------------|------------------------|------------------------------|---------------------------------------|------------------------|
| HP_APM_CTRL    | HP_APM_REG       | 4                      | HP_APM_ FUNC_CTRL_REG        | 16                                    | HP_APM_REGION_FILTER_EN_REG |
| LP_APM_CTRL    | LP_APM_REG       | 1                      | LP_APM_ FUNC_CTRL_REG        | 4                                     | LP_APM_REGION_FILTER_EN_REG |
| CPU_APM_CTRL   | CPU_APM_REG      | 2                      | CPU_APM_ FUNC_CTRL_REG       | 8                                     | CPU_APM_REGION_FILTER_EN_REG |
```

### 16.5.2.2 Address Ranges

* The `HP_APM_REG` register module configures up to 16 address ranges (i.e., region n, n=0-15) for `HP_APM_CTRL`. The start and end address of each region (address range) are configured by `HP_APM_REGIONn_ADDR_START` and `HP_APM_REGIONn_ADDR_END`, respectively. Configure the bit n of `HP_APM_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.
* The `LP_APM_REG` register module configures up to four address ranges (i.e., region n, n=0-3) for `LP_APM_CTRL`. The start and end address of each region are configured by `LP_APM_REGIONn_ADDR_START` and `LP_APM_REGIONn_ADDR_END`. Configure the bit n of `LP_APM_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.
* The `CPU_APM_REG` register module configures up to eight address ranges (i.e., region n, n=0-7) for `CPU_APM_CTRL`. The start and end address of each region are configured by `CPU_APM_REGIONn_ADDR_START` and `CPU_APM_REGIONn_ADDR_END`. Configure the bit n of `CPU_APM_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.

When configuring the address ranges, the address requires a 4-byte alignment (the lower two bits of the address are 0). For example, the address range could be set to `0x4080000C ~ 0x40808774` or `0x600C0008 ~ 0x600CFF70`.

### 16.5.2.3 Access Permissions of Address Ranges

For each address range, the access permissions (read/write/execute) are configurable in different security modes:

* Masters in TEE mode always have read, write, and execute permissions in the address range.
* For masters in REEO, REE1 or REE2 mode, access permissions are configured with `HP_APM_REGIONn_ATTR_REG`, `LP_APM_REGIONn_ATTR_REG`, or `CPU_APM_REGIONn_ATTR_REG` depending on the access path.
```