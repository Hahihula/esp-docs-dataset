

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
GoBack

- Configure data bus region 1 with ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MAX_REG.
- Configure peripheral bus region 0 with ASSIST_DEBUG_CORE_O_AREA_PIF_O_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_O_MAX_REG.
- Configure peripheral bus region 1 with ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG.
- Configure SP monitored region with ASSIST_DEBUG_CORE_O_SP_MIN_REG and ASSIST_DEBUG_CORE_O_SP_MAX_REG.

2. Configure interrupts.
- Configure ASSIST_DEBUG_CORE_O_INTR_ENA_REG to enable the interrupt of a monitoring mode.
- Configure ASSIST_DEBUG_CORE_O_INTR_RAW_REG to get the interrupt status of a monitoring mode.
- Configure ASSIST_DEBUG_CORE_O_INTR_CLR_REG to clear the interrupt of a monitoring mode.

3. Configure ASSIST_DEBUG_CORE_O_MONTR_ENA_REG to enable the monitoring mode(s). Various monitoring modes can be enabled at the same time.

Assuming that Debug Assistant module needs to monitor whether data bus writes to [A–B] address space, you can enable monitoring in either data bus region 0 or region 1. The following configuration process is based on region 0:

1. Configure ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN to 1 to enable CPU to update PC signals to the Debug Assistant module.
2. Configure ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG to Address A.
3. Configure ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG to Address B.
4. Configure ASSIST_DEBUG_CORE_O_INTR_ENA_REG bit[1] to enable the interrupt for write operations by data bus in region 0.
5. Configure ASSIST_DEBUG_CORE_O_MONTR_ENA_REG bit[1] to enable monitoring write operations by data bus in region 0.
6. Configure interrupt matrix to map ASSIST_DEBUG_INT into CPU interrupt (please refer to Chapter 9 Interrupt Matrix (INTMTX)).

7. After the interrupt is triggered:
- Read ASSIST_DEBUG_CORE_O_INTR_RAW_REG to obtain which operation triggered the interrupt.
- If the interrupt is triggered by region monitoring, read ASSIST_DEBUG_CORE_O_AREA_PC_REG for the PC value, and ASSIST_DEBUG_CORE_O_AREA_SP_REG for the SP.
- If the interrupt is triggered by stack monitoring, read ASSIST_DEBUG_CORE_O_SP_PC_REG for the PC value.
- Write 1 to the corresponding bits of ASSIST_DEBUG_CORE_O_INTR_RAW_REG to clear the interrupts.

Espressif Systems
544
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```