

```markdown
## 9.8 Registers

The addresses in this section are relative to low-power management base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 9.1. RTC_CNTL_OPTIONSO_REG (0x0000)

RTC_CNTL_SW_STALL_PROCPU_CO When RTC_CNTL_SW_STALL_PROCPU_C1 is configured to 0x21, setting this bit to 0x2 stalls the CPU by SW. (R/W)

RTC_CNTL_SW_PROCPU_RST Set this bit to reset the CPU by SW. (WO)

RTC_CNTL_BB_I2C_FORCE_PD Set this bit to FPD BB_I2C. (R/W)

RTC_CNTL_BB_I2C_FORCE_PU Set this bit to FPU BB_I2C. (R/W)

RTC_CNTL_BBPLL_I2C_FORCE_PD Set this bit to FPD BB_PLL_I2C. (R/W)

RTC_CNTL_BBPLL_I2C_FORCE_PU Set this bit to FPU BB_PLL_I2C. (R/W)

RTC_CNTL_BBPLL_FORCE_PD Set this bit to FPD BB_PLL. (R/W)

RTC_CNTL_BBPLL_FORCE_PU Set this bit to FPU BB_PLL. (R/W)

RTC_CNTL_XTL_FORCE_PD Set this bit to FPD the crystal oscillator. (R/W)

RTC_CNTL_XTL_FORCE_PU Set this bit to FPU the crystal oscillator. (R/W)

RTC_CNTL_DG_WRAP_FORCE_RST Set this bit to force reset the digital system in deep-sleep. (R/W)

RTC_CNTL_DG_WRAP_FORCE_NORST Set this bit to disable force reset to digital system in deep-sleep. (R/W)

RTC_CNTL_SW_SYS_RST Set this bit to reset the system via SW. (WO)
```