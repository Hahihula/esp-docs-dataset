

```markdown
4. Configure `HP_APM_REGIONn_ATTR_REG`, `LP_APM_REGIONn_ATTR_REG`, or `CPU_APM_REGIONn_ATTR_REG` to set the access permissions for each region.
5. Configure bit `n` of `HP_APM_REGION_FILTER_EN_REG`, `LP_APM_REGION_FILTER_EN_REG`, or `CPU_APM_REGION_FILTER_EN_REG` to enable permission checks for the corresponding address range.
6. Configure `HP_APM_FUNC_CTRL_REG`, `LP_APM_FUNC_CTRL_REG`, or `CPU_APM_FUNC_CTRL_REG` to enable the permission management for different access paths (enabled by default).

Take I2S accessing HP SRAM via GDMA as an example, assuming that it is only allowed to read and write in the fourth address range 0x40805000 ~ 0x4080FFFF:

1. Configure the HP CPU to machine mode (i.e., TEE mode).
2. According to the master ID number in Table 16.5-1, set `TEE_M19_MODE` to 1, so that the security mode for I2S access via GDMA is REEO.
3. Configure `HP_APM_REGION3_ADDR_START` to 0x40805000 and `HP_APM_REGION3_ADDR_END` to 0x4080EFFECT, respectively.
4. Set `HP_APM_REGION3_RO_W` and `HP_APM_REGION3_RO_R` to 1 to enable the access permissions to the address range.
5. Set bit 3 of `HP_APM_REGION_FILTER_EN` to 1 to enable region 3 (i.e., the fourth address range).
6. Set `HP_APM_M1_FUNC_EN` to 1 to enable the permission management for HP_APM_CTRL M1.

Through this configuration, I2S can read and write in the address range of 0x40805000 to 0x4080FFFF in HP SRAM using GDMA.
```

## 16.7 Illegal Access and Interrupts

If the information carried on the bus is inconsistent with the configuration, ESP32-C61 will regard it as an illegal access and proceed as follows:

- Denies the access request and returns the default value:
    - Returns 0 on instruction execution and read operations
    - Invalidate write operations
- Triggers interrupt

The APM controller will automatically record relevant information about the illegal access, including the master ID, security mode, access address, reasons for illegal access (address out of bounds or permission restrictions), and permission management result of each access path. All this information is obtained from relevant registers listed in Section 16.8 Register Summary.

Take the access path `HP_APM_CTRL MO` as an example. When an illegal access occurs:

- `HP_APM_MO_EXCEPTION_ID` records the master ID.
- `HP_APM_MO_EXCEPTION_MODE` records the security mode.
- `HP_APM_MO_EXCEPTION_ADDR` records the access address.
- `HP_APM_MO_EXCEPTION_STATUS` records the reason for illegal access.
```