

```markdown
- ASSIST_DEBUG_CORE_0_AREA_PIF_1_WR_INT: Triggered when the HP CPUO Peripheral bus writes in HP CPUO region 1.
- ASSIST_DEBUG_CORE_0_SP_SPILL_MIN_INT: Triggered when the HP CPUO SP goes below the lower bound of the HP CPUO SP monitored region.
- ASSIST_DEBUG_CORE_0_SP_SPILL_MAX_INT: Triggered when the HP CPUO SP goes beyond the upper bound of the HP CPUO SP monitored region.
- ASSIST_DEBUG_CORE_1_AREA_DRAMO_O_RD_INT: Triggered when the HP CPU1 Data bus reads in HP CPU1 region 0.
- ASSIST_DEBUG_CORE_1_AREA_DRAMO_O_WR_INT: Triggered when the HP CPU1 Data bus writes in HP CPU1 region 0.
- ASSIST_DEBUG_CORE_1_AREA_DRAMO_1_RD_INT: Triggered when the HP CPU1 Data bus reads in HP CPU1 region 1.
- ASSIST_DEBUG_CORE_1_AREA_DRAMO_1_WR_INT: Triggered when the HP CPU1 Data bus writes in HP CPU1 region 1.
- ASSIST_DEBUG_CORE_1_AREA_PIF_O_RD_INT: Triggered when the HP CPU1 Peripheral bus reads in HP CPU1 region 0.
- ASSIST_DEBUG_CORE_1_AREA_PIF_O_WR_INT: Triggered when the HP CPU1 Peripheral bus writes in HP CPU1 region 0.
- ASSIST_DEBUG_CORE_1_AREA_PIF_1_RD_INT: Triggered when the HP CPU1 Peripheral bus reads in HP CPU1 region 1.
- ASSIST_DEBUG_CORE_1_AREA_PIF_1_WR_INT: Triggered when the HP CPU1 Peripheral bus writes in HP CPU1 region 1.
- ASSIST_DEBUG_CORE_1_SP_SPILL_MIN_INT: Triggered when the HP CPU1 SP goes below the lower bound of the HP CPU1 SP monitored region.
- ASSIST_DEBUG_CORE_1_SP_SPILL_MAX_INT: Triggered when the HP CPU1 SP goes beyond the upper bound of the HP CPU1 SP monitored region.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 21.6 Register Summary.

## 21.5 Recommended Operation

### 21.5.1 Region Monitoring and SP Monitoring Configuration

The Debug Assistant module can monitor reads and writes performed by the Data bus and Peripheral bus of HP CPUO and HP CPU1. Two memory regions on each bus can be monitored at the same time. All the
```