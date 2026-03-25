

```markdown
## Register 18.4. LP_ANA_FIB_ENABLE_REG (0x000C)

LP_ANA_ANA_FIB_ENA Controls the enabling of the voltage glitch detectors. Bit2, bit3, bit4, bit5 correspond to VDDPST2/3, VDDPST1, VDDA3, and VDDA8, respectively.
- 0: Controlled by LP_ANA_PWR_GLITCH_RESET_ENA
- 1: Forcibly enabled by hardware (R/W)

## Register 18.5. LP_ANA_INT_RAW_REG (0x0010)

LP_ANA_BOD_MODEO_INT_RAW The raw interrupt status of LP_ANA_BOD_MODEO_INT. (R/WTC/SS)

## Register 18.6. LP_ANA_INT_ST_REG (0x0014)

LP_ANA_BOD_MODEO_INT_ST The masked interrupt status of LP_ANA_BOD_MODEO_INT. (RO)
```