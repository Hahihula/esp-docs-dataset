

```markdown
| APM Controllers | Register Modules | Number of Access Paths | Enable Permission Management | Number of Configurable Address Ranges | Enable Address Ranges |
|-----------------|------------------|------------------------|------------------------------|---------------------------------------|------------------------|
| HP_APM_CTRL     | HP_APM_REG       | 5                      | `HP_APM_FUNC_CTRL_REG`      | 16                                    | `HP_APM_REGION_FILTER_EN_REG` |
| LP_APMO_CTRL    | LP_APMO_REG      | 1                      | `LP_APMO_FUNC_CTRL_REG`     | 8                                     | `LP_APMO_REGION_FILTER_EN_REG` |
| LP_APM_CTRL     | LP_APM_REG       | 2                      | `LP_APM_FUNC_CTRL_REG`      | 8                                     | `LP_APM_REGION_FILTER_EN_REG` |
| CPU_APM_CTRL    | CPU_APM_REG      | 4                      | `CPU_APM_FUNC_CTRL_REG`     | 8                                     | `CPU_APM_REGION_FILTER_EN_REG` |
| HP_PERI_APM_CTRL| TEE_REG          | Same as the number of HP system register modules | N/A                         | Same as the number of HP system register modules | N/A                    |
| LP_PERI_APM_CTRL| LP_TEE_REG       | Same as the number of LP system register modules | N/A                         | Same as the number of LP system register modules | N/A                    |
```

#### 18.5.2.2 SYS_APM Controller

##### 18.5.2.2.1 Address Ranges

*   `HP_APM_REG` register module can configure up to 16 address ranges (i.e., region n, n=0-15) for HP_APM_CTRL. The start and end addresses of each region (address range) are configured by `HP_APM_REGIONn_ADDR_START` and `HP_APM_REGIONn_ADDR_END`, respectively. Configure the bit n of `HP_APM_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.
*   `LP_APMO_REG` register module can configure up to eight address ranges (i.e., region n, n=0-7) for LP_APMO_CTRL. The start and end addresses of each region are configured by `LP_APMO_REGIONn_ADDR_START` and `LP_APMO_REGIONn_ADDR_END`. Configure the bit n of `LP_APMO_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.
*   `LP_APM_REG` register module can configure up to eight address ranges (i.e., region n, n=0-7) for LP_APM_CTRL. The start and end addresses of each region are configured by `LP_APM_REGIONn_ADDR_START` and `LP_APM_REGIONn_ADDR_END`. Configure the bit n of `LP_APM_REGION_FILTER_EN_REG` to enable region n. Region 0 (i.e., the first address range) is enabled by default.
*   `CPU_APM_REG` register module can configure up to eight address ranges (i.e., region n, n=0-7) for
```