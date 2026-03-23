

```markdown
Chapter 12 Low-Power Management

Register 12.81. LP_ANA_BOD_MODE1_CNTL_REG (0x0004)

LP_ANA_BOD_MODE1_RESET_ENA

(reserved)

31 | 30
--+-----------------------------------------------
| Reset

LP_ANA_BOD_MODE1_RESET_ENA Configures whether to enable brownout detector mode 1.
0: Disable
1: Enable
(R/W)

Register 12.82. LP_ANA_FIB_ENABLE_REG (0x000C)

LP_ANA_ANA_FIB_ENA

31 | 0
--+-------------------------
| Reset

LP_ANA_ANA_FIB_ENA FIB (Focused Ion Beam) selection register. (R/W)

Register 12.83. LP_ANA_INT_RAW_REG (0x0010)

LP_ANA_BOD_MODEO_INT_RAW

(reserved)

31 | 30
--+-----------------------------------------------
| Reset

LP_ANA_BOD_MODEO_INT_RAW The raw interrupt status of LP_ANA_BOD_MODEO_INT.
(R/WTC/SS)
```