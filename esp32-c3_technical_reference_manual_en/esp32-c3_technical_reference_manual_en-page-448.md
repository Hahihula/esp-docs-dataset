

```markdown
- Configure Data bus region 1 with ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MAX_REG.
- Configure Peripheral bus region 0 with ASSIST_DEBUG_CORE_O_AREA_PIF_O_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_O_MAX_REG.
- Configure Peripheral bus region 1 with ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG and ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG.
- Configure SP threshold with ASSIST_DEBUG_CORE_O_SP_MIN_REG and ASSIST_DEBUG_CORE_O_SP_MAX_REG.

2. Configure interrupts.
    - Configure ASSIST_DEBUG_CORE_O_INTR_ENA_REG to enable the interrupt of a monitoring mode.
    - Configure ASSIST_DEBUG_CORE_O_INTR_RAW_REG to get the interrupt status of a monitoring mode.
    - Configure ASSIST_DEBUG_CORE_O_INTR_CLR_REG to clear the interrupt of a monitoring mode.

3. Configure ASSIST_DEBUG_CORE_O_MONTR_ENA_REG to enable the monitoring mode(s). Various monitoring modes can be enabled at the same time.

Assuming that Debug Assistant needs to monitor whether Data bus has written to [A ~ B] address space, the user can enable monitoring in either Data bus region 0 or region 1. The following configuration process is based on region 0:

1. Configure ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG to A.
2. Configure ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG to B.
3. Configure ASSIST_DEBUG_CORE_O_INTR_ENA_REG bit[1] to enable the interrupt for write operations by Data bus in region 0.
4. Configure ASSIST_DEBUG_CORE_O_MONTR_ENA_REG bit[1] to enable monitoring write operations by Data bus in region 0.
5. Configure interrupt matrix to map ASSIST_DEBUG_INT into CPU interrupt (please refer to Chapter 8 Interrupt Matrix (INTERRUPT)).

6. After the interrupt is triggered:
    - Read ASSIST_DEBUG_CORE_O_INTR_RAW_REG to learn which operation triggered interrupt.
    - If the interrupt is triggered by region monitoring, read ASSIST_DEBUG_CORE_O_AREA_PC_REG for the PC value, and ASSIST_DEBUG_CORE_O_AREA_SP_REG for the SP.
    - If the interrupt is triggered by stack monitoring, read ASSIST_DEBUG_CORE_O_SP_PC_REG for the PC value.
    - Write '1' to the corresponding bits of ASSIST_DEBUG_CORE_O_INTR_RAW_REG to clear the interrupts.

## 17.4.2 PC Logging Configuration Process

The CPU sends PC signals to Debug Assistant. Only when ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN is 1, the PC signal is valid, otherwise, it is always 0.
```