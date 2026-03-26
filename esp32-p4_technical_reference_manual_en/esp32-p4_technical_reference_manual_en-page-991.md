

```markdown
PMU_n1_VDBBAT_MODE is 1, the battery power is enabled and can be used in Deep-sleep mode, where the main power, including VDD_ANA, is cut off, and only the LP AON & PMU power domains are powered up.

### 14.4.2.9 Output Regulator Control

As shown in Figure 14.4-1, ESP32-P4 has four output regulators:

*   VDDO_FLASH (VO1), typically used for on-chip flash voltage regulation
*   VDDO_PSRAM (VO2), typically used for on-chip PSRAM voltage regulation
*   VDDO_3 (VO3) and VDDO_4 (VO4), which convert the input VDD_LDO (typically 3.3 V) into the voltages needed by peripherals such as flash, PSRAM, MIPI, and SDIO.

#### 14.4.2.9.1 Regulator Features

The regulators support the following features:

*   Supports LDO mode and bypass mode. LDO mode supports an output of 0.5 V – 2.7 V, while bypass mode outputs the voltage of VDD_LDO. Mode selection is controlled by a hardware state machine or a register, with the control authority managed by a register. The flash regulator (VO1) also supports eFuse control.

    -   The mode control for VO1 is shown in Figure 14.4-3. In the figure, TIEH_SEL on the right being 0 selects LDO mode; being 1 selects bypass mode.

        ```markdown
        EFUSE_OP1A_TIEH_SEL_O ──┬── PMU_OP1A_FORCE_TIEH_SEL_O
                                 │
                                 ├─┐
                                 │ 1
                                 ├─┼─→ (MUX)
                                 │   │
         PMU_OP1A_TIEH_SEL_O      │   │
                                 │   ├─ 0 ─── TIEH_SEL
                                 │   │
         PMU_OP1A_TIEH_O          │   ├─ 2
                                 │   │
         SDMMC_O                   │   ├─ 3
                                 │   │
         1                         │   │
         SDMMC_1                    └───┘
        ```

        Figure 14.4-3. VO1 Mode Control

    -   The mode control for VO2/3/4 is shown in Figure 14.4-4. In the figure, TIEH_SEL on the right being 0 selects LDO mode; being 1 selects bypass mode.
```