

```markdown
| Regulators | Over-Current Protection Control Registers |
|------------|---------------------------------------------|
| VO1        | FSM or PMU_ANA_OP1A_EN_CUR_LIM_0          |
| VO2        | PMU_ANA_OP1A_EN_CUR_LIM_1                  |
| VO3        | PMU_ANA_OP2A_EN_CUR_LIM_0                  |
| VO4        | PMU_ANA_OP2A_EN_CUR_LIM_1                  |

Table 14.4-6. Regulator Waiting Counter
| Regulators | Counter Target 1                            | Counter Target 2                          |
|------------|---------------------------------------------|-------------------------------------------|
| VO1        | PMU_OP1A_TARGETO_0[6:0]                     | PMU_OP1A_TARGET1_0[7:0]                   |
| VO2        | PMU_OP1A_TARGET1_0[7:0]                     | PMU_OP1A_TARGET1_1[7:0]                   |
| VO3        | PMU_OP2A_TARGETO_0[7:0]                     | PMU_OP2A_TARGET1_0[7:0]                   |
| VO4        | PMU_OP2A_TARGET1_0[7:0]                     | PMU_OP2A_TARGET1_1[7:0]                   |

Note:
1. The bit 7 of `PMU_OP1A_TARGETO_0` clears the counter. Setting bit 7 to 1 resets the counter.
2. The counter clock is derived from LP_DYN_SLOW_CLK, which is divided by a factor of 16.

#### 14.4.2.9.2 Regulator Configuration Examples

- **Example 1: VO3 powering MIPI D-PHY (2.5 V, LDO mode)**
  On the board, the VO3 pin is connected to `VDD_MIPI_DPHY` that requires 2.5 V operating voltage.
  In this scenario, select LDO mode and set `VOUT = 2.5 V`. One valid combination is `VREF = 1.0 V (DREF=9)` and `MUL = 2.5 (MUL=6)`, i.e., `PMU_ANA_0P2A_DREF_0=9, PMU_ANA_0P2A_MUL_0=6`, and set `PMU_0P2A_TIEH_0=0` (LDO).

- **Example 2: VO4 powering VDD_IO_5 (SD card voltage switching)**
  In reference designs, VO4 may be connected to `VDD_IO_5` to supply some GPIO/SDIO pins.
  - 3.3 V output: use bypass mode (for example, set `PMU_0P2A_TIEH_1=1`).
  - 1.8 V output: use LDO mode and set `VOUT = 1.8 V`. One valid combination is `VREF = 0.9 V (DREF=8)` and `MUL = 2.0 (MUL=4)`, i.e., `PMU_ANA_0P2A_DREF_1=8, PMU_ANA_0P2A_MUL_1=4`, and set `PMU_0P2A_TIEH_1=0` (LDO).

#### 14.4.2.9.3 Software Configuration Steps

The recommended software configuration steps (example) are as follows:

1. Configure output mode: set `PMU_0PxA_FORCE_TIEH_SEL_y` so the register controls mode selection, then choose LDO or bypass mode via
   `PMU_0PxAxA_TIEH_SEL_y/PMU_0PxAxA_TIEH_y` (see Table 14.4-3).
```