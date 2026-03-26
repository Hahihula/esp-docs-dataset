
```markdown
| Regulators | PMU_OPxA_FORCE_TIEH_SEL_y | PMU_OPxA_TIEH_SEL_y | PMU_OPxA_TIEH_y |
|------------|----------------------------|----------------------|-----------------|
| VO2        | PMU_OP1A_FORCE_TIEH_SEL_1 | PMU_OP1A_TIEH_SEL_1  | PMU_OP1A_TIEH_1 |
| VO3        | PMU_OP2A_FORCE_TIEH_SEL_O | PMU_OP2A_TIEH_SEL_O  | PMU_OP2A_TIEH_O |
| VO4        | PMU_OP2A_FORCE_TIEH_SEL_1 | PMU_OP2A_TIEH_SEL_1  | PMU_OP2A_TIEH_1 |

- Supports LDO output voltage setting: In LDO mode, the output voltage is configured by analog registers `PMU_ANA_0PxA_DREF_y` (sets Vref) and `PMU_ANA_0PxA_MUL_y` (sets MUL), following `VOUT = MUL × VREF`. Vref supports 0.5 V–1.6 V, and MUL supports 1.0–2.75 (step 0.25). For details, see field descriptions in `PMU_EXT_LDO_PO_OP1A_ANA_REG`, `PMU_EXT_LDO_PO_OP2A_ANA_REG`.
- Supports switch control. Only the flash voltage regulator (VO1) supports power control by the PMU state machine; the other regulators only support power control by software. The regulator is enabled when the register in Table 14.4-4 is set to 1; otherwise, the regulator is disabled.

| Regulator | Power Control |
|-----------|---------------|
| VO1       | `PMU_n1_REGULATOR_VO1_XPD` |
| VO2       | `PMU_OP1A_XPD_1` |
| VO3       | `PMU_OP2A_XPD_O` |
| VO4       | `PMU_OP2A_XPD_1` |

- Over-current protection: Before powering up the regulators, users have the option to enable the over-current protection function to prevent excessive transient current that may damage the capacitor. After the capacitor charging is complete, the over-current protection should be disabled. The capacitor charging time depends on the load capacitance and voltage, following `Tms = CF×VV / 50`. Table 14.4-5 provides the over-current protection enable registers; when the register is set to 1, the function is enabled; otherwise, it is disabled.
```