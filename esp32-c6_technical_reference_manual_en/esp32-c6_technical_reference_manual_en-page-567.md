

```markdown
- Configure the HP CPU to machine mode (ie. TEE mode).
- According to the ID number in the table 18.4-5, set the TEE_M19_MODE to be 1, so as to set the security mode for I2S access via GDMA to REEO mode.
- Configure the start address to 0x40805000 and end address to 0x4080F000 for the access address range by configuring HP_APM_REGION3_ADDR_START and HP_APM_REGION3_ADDR_END respectively.
- Set HP_APM_REGION3_RO_W and HP_APM_REGION3_RO_R to 1.
- Set the bit 3 of HP_APM_REGION_FILTER_EN to 1.
- Set HP_APM_M1_FUNC_EN to 1.

Through the above configuration, I2S can read and write in the address range of 0x40805000 ~ 0x4080F000 in HP_MEM via GDMA.

## 16.5 Illegal access and interrupts

If the information carried on the bus is inconsistent with the configuration, ESP32-C6 will regard it as an illegal access and proceed as follows:

- Deny the access request and return the default value:
    - Returns 0 on instruction execution and read
    - Invalidate the write operation
- Trigger interrupt

The APM controller module will automatically record relevant information about illegal access, including master ID, security mode, access address, reason for illegal access (address out of bounds or permission restrictions), and permission management result of each access path. All these information can be obtained from relevant registers listed in the section 16.6 Register Summary.

Take the access path HP_APM_MO as an example. When illegal access occurs:

- `HP_APM_MO_EXCEPTION_ID` records the master ID.
- `HP_APM_MO_EXCEPTION_MODE` records the security mode.
- `HP_APM_MO_EXCEPTION_ADDR` records the access address.
- `HP_APM_MO_EXCEPTION_STATUS` records the reason for illegal access.

    - If the address requested to access is not among the enabled region of the 16 address ranges configured by HP_APM_REGIONn_ADDR_START, HP_APM_REGIONn_ADDR_END and HP_APM_REGION_FILTER_EN, bit1 of HP_APM_MO_EXCEPTION_STATUS will be set to 1, indicating address out of bounds.
    - If the address requested to access is among the enabled region/regions of the 16 address ranges but the master doesn't have the read/write/execute permission within this region/regions, then the bit0 will be set to 1, indicating permission restrictions.

- `HP_APM_MO_EXCEPTION_REGION` records the permission management result of each address range.

This register has a total of 16 bits, corresponding to 16 groups of address ranges, and bit0 corresponds to the first group of address ranges. When the address to access is within a particular enabled address
```