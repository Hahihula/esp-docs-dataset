

```markdown
Chapter 21 Debug Assistant

monitoring modes supported by the Debug Assistant module are listed below:

- Monitoring the read/write operations performed by Data bus
    - HP CPUO Data bus reads in HP CPUO region 0
    - HP CPUO Data bus writes in HP CPUO region 0
    - HP CPUO Data bus reads in HP CPUO region 1
    - HP CPUO Data bus writes in HP CPUO region 1
    - HP CPU1 Data bus reads in HP CPU1 region 0
    - HP CPU1 Data bus writes in HP CPU1 region 0
    - HP CPU1 Data bus reads in HP CPU1 region 1
    - HP CPU1 Data bus writes in HP CPU1 region 1

- Monitoring the read/write operations performed by Peripheral bus
    - HP CPUO Peripheral bus reads in HP CPUO region 0
    - HP CPUO Peripheral bus writes in HP CPUO region 0
    - HP CPUO Peripheral bus reads in HP CPUO region 1
    - HP CPUO Peripheral bus writes in HP CPUO region 1
    - HP CPU1 Peripheral bus reads in HP CPU1 region 0
    - HP CPU1 Peripheral bus writes in HP CPU1 region 0
    - HP CPU1 Peripheral bus reads in HP CPU1 region 1
    - HP CPU1 Peripheral bus writes in HP CPU1 region 1

- Monitoring SP bounds violations
    - HP CPUO SP goes beyond the upper bound of the HP CPUO SP monitored region
    - HP CPUO SP goes below the lower bound of the HP CPUO SP monitored region
    - HP CPU1 SP goes beyond the upper bound of the HP CPU1 SP monitored region
    - HP CPU1 SP goes below the lower bound of the HP CPU1 SP monitored region

The configuration process for region monitoring and SP monitoring is as follows:

1. Configure the monitored region and SP bounds.
    - Configure HP CPUO Data bus region 0 with ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG.
    - Configure HP CPUO Data bus region 1 with ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MAX_REG.
    - Configure HP CPUO Peripheral bus region 0 with ASSIST_DEBUG_CORE_O_AREA_PIF_O_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_O_MAX_REG.
    - Configure HP CPUO Peripheral bus region 1 with ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG.
```