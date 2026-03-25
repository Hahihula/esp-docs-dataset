

```markdown
- BUS_MONITOR_CORE_O_AREA_DRAMO_O_WR_INT: Triggered when the HP CPU Data bus writes to HP CPU region 0.
- BUS_MONITOR_CORE_O_AREA_DRAMO_1_RD_INT: Triggered when the HP CPU Data bus reads from HP CPU region 1.
- BUS_MONITOR_CORE_O_AREA_DRAMO_1_WR_INT: Triggered when the HP CPU Data bus writes to HP CPU region 1.
- BUS_MONITOR_CORE_O_AREA_PIF_O_RD_INT: Triggered when the HP CPU Peripheral bus reads from HP CPU region 0.
- BUS_MONITOR_CORE_O_AREA_PIF_O_WR_INT: Triggered when the HP CPU Peripheral bus writes to HP CPU region 0.
- BUS_MONITOR_CORE_O_AREA_PIF_1_RD_INT: Triggered when the HP CPU Peripheral bus reads from HP CPU region 1.
- BUS_MONITOR_CORE_O_AREA_PIF_1_WR_INT: Triggered when the HP CPU Peripheral bus writes to HP CPU region 1.
- BUS_MONITOR_CORE_O_SP_SPILL_MIN_INT: Triggered when the HP CPU SP goes below the lower bound of the HP CPU SP monitored region.
- BUS_MONITOR_CORE_O_SP_SPILL_MAX_INT: Triggered when the HP CPU SP goes beyond the upper bound of the HP CPU SP monitored region.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 Interrupt Matrix > Section 11.2 Terminology.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 20.6 Register Summary.

## 20.5 Programming Procedures

### 20.5.1 Region Monitoring and SP Monitoring Configuration

The configuration process for region monitoring and SP monitoring is as follows:

1. Configure the monitored region and SP bounds.
    - Configure the HP CPU Data bus region 0 with BUS_MONITOR_CORE_O_AREA_DRAMO_O_MIN_REG and BUS_MONITOR_CORE_O_AREA_DRAMO_O_MAX_REG.
    - Configure the HP CPU Data bus region 1 with BUS_MONITOR_CORE_O_AREA_DRAMO_1_MIN_REG and BUS_MONITOR_CORE_O_AREA_DRAMO_1_MAX_REG.
    - Configure the HP CPU Peripheral bus region 0 with BUS_MONITOR_CORE_O_AREA_PIF_O_MIN_REG and BUS_MONITOR_CORE_O_AREA_PIF_O_MAX_REG.
```