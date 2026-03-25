

```markdown
Note:

* When powered up, only the CPU is in TEE mode by default, and the other masters are in REE2 mode. By default, the APM controller blocks access requests from all masters in REEO, REE1, and REE2 modes.
* All registers listed in 15.7 Register Summary can only be configured by the masters that are in TEE security mode.

## 15.5 Programming Procedure

For a master to access memory or peripheral registers, follow the programming procedures below:

1. Set the CPU to machine mode (i.e., TEE mode).
2. Choose the security mode of the master by configuring `TEE_Mn_MODE`. The master ID `n` is defined in Table 15.4-1.
3. Configure the start and end address for access address ranges by setting
   `HP_APM_REGIONn_ADDR_START`, `HP_APM_REGIONn_ADDR_END`, or
   `LP_APM_REGIONn_ADDR_START`, `LP_APM_REGIONn_ADDR_END`.
4. Configure the access permissions of each region by configuring `HP_APM_REGIONn_ATTR_REG` or
   `LP_APM_REGIONn_ATTR_REG`.
5. Set the bit `n` of `HP_APM_REGION_FILTER_EN_REG` or `LP_APM_REGION_FILTER_EN_REG` to enable region `n`.
6. Configure `HP_APM_FUNC_CTRL_REG` or `LP_APM_FUNC_CTRL_REG` to enable permission management of different access paths (enabled by default).

Take I2S accessing HP SRAM via GDMA as an example, assuming that it is only allowed to read and write in the fourth address range 0x40805000 ~ 0x4080F000:

1. Configure the CPU to machine mode (ie. TEE mode).
2. According to the master ID number in Table 15.4-1, set `TEE_M19_MODE` to be 1, so that the security mode for I2S access via GDMA is REEO.
3. Configure `HP_APM_REGION3_ADDR_START` to 0x40805000 and `HP_APM_REGION3_ADDR_END` to 0x4080F000, respectively.
4. Set `HP_APM_REGION3_RO_W` and `HP_APM_REGION3_RO_R` to 1.
5. Set the bit 3 of `HP_APM_REGION_FILTER_EN` to 1.
6. Set `HP_APM_M1_FUNC_EN` to 1.

## 15.6 Illegal Access and Interrupts

If the information carried on the bus is inconsistent with the configuration, ESP32-H2 will regard it as an illegal access and proceed as follows:

* Denies the access request and returns the default value:
    - Returns 0 on instruction execution and read operations
```