

```markdown
- LP_APMO_MO_INTR
- CPU_APM_MO_INTR
- CPU_APM_M1_INTR
- CPU_APM_M2_INTR
- CPU_APM_M3_INTR
```

Each interrupt is configured with an interrupt enable register APM_INT_EN and an interrupt clear register EXCEPTION_STATUS_CLR. When the interrupt enable register is set to 1, if an illegal access occurs on a controlled access path, the corresponding interrupt will be generated. Configuring the interrupt clear register clears the interrupt signal until the next illegal access occurs.

## 18.6.2 PERI_APM Controller

When the information carried on the bus does not match the configuration, ESP32-C5 treats it as an illegal access and handles it as follows:

- Rejects the access request and returns a default value, specifically:
    - Returns 0 for read and execute operations
    - Ignores write operations
- Returns an error message to the master via the bus, causing the master to enter an exception state

Setting HP/LP_BUS_ERR_RESP_EN to 1 enables returning an error message on illegal access.

The PERI_APM controller does not log information related to illegal access.

## 18.7 Programming Procedure

For a master to access memory or peripheral registers, follow the programming procedures below:

1. Set the HP CPU to the machine mode (i.e., TEE mode).

2. Configure `TEE_Mn_MODE` or `LP_TEE_Mn_MODE` to choose the security mode for the master. The master ID *n* is defined in Table 18.5-1.

3. Configure `HP_APM_REGIONn_ADDR_START` and `HP_APM_REGIONn_ADDR_END`, or `LP_APM_REGIONn_ADDR_START` and `LP_APM_REGIONn_ADDR_END`, or `LP_APMO_REGIONn_ADDR_START` and `LP_APMO_REGIONn_ADDR_END`, or `CPU_APM_REGIONn_ADDR_START` and `CPU_APM_REGIONn_ADDR_END` to define the start and end address of the access address ranges.

4. Configure `HP_APM_REGIONn_ATTR_REG`, or `LP_APM_REGIONn_ATTR_REG`, or `LP_APMO_REGIONn_ATTR_REG`, or `CPU_APM_REGIONn_ATTR_REG` to set the access permissions of each region.

5. Configure `HP_APM_REGION_FILTER_EN_REG`, or `LP_APM_REGION_FILTER_EN_REG`, or `LP_APMO_REGION_FILTER_EN_REG`, or `CPU_APM_REGION_FILTER_EN_REG` to enable region *n*.
```