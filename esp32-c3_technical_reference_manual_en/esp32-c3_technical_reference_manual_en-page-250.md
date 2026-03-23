

```markdown
Register 9.29. RTC_CNTL_DIG_PWC_REG (0x0088)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

RTC_CNTL_VDD_SPI_PWR_DRV Configures the vdd_spi's drive intensity. (R/W)

RTC_CNTL_VDD_SPI_PWR_FORCE Set this bit to allow software to configure vdd_spi's drive intensity. (R/W)

RTC_CNTL_LSLP_MEM_FORCE_PD Set this bit to force the memories in the digital system not to enter retention mode in sleep. (R/W)

RTC_CNTL_LSLP_MEM_FORCE_PU Set this bit to force the memories in the digital system into retention mode in sleep. (R/W)

RTC_CNTL_DG_PERI_FORCE_PD Set this bit to FPD the digital peripherals. (R/W)

RTC_CNTL_DG_PERI_FORCE_PU Set this bit to FPU the digital peripherals. (R/W)

RTC_CNTL_FASTMEM_FORCE_LPD Set this bit to force the fast memory not to enter retention mode in sleep. (R/W)

RTC_CNTL_FASTMEM_FORCE_LPU Set this bit to force the fast memory into retention mode in sleep. (R/W)

RTC_CNTL_WIFI_FORCE_PD Set this bit to FPD wireless. (R/W)

RTC_CNTL_WIFI_FORCE_PU Set this bit to FPU wireless. (R/W)

RTC_CNTL_DG_WRAP_FORCE_PD Set this bit to FPD the digital system. (R/W)

RTC_CNTL_DG_WRAP_FORCE_PU Set this bit to FPU the digital system. (R/W)

RTC_CNTL_CPU_TOP_FORCE_PD Set this bit to FPD the CPU. (R/W)

RTC_CNTL_CPU_TOP_FORCE_PU Set this bit to FPU the CPU. (R/W)

RTC_CNTL_DG_PERI_PD_EN Set this bit to enable FPD digital peripherals in sleep. (R/W)

RTC_CNTL_CPU_TOP_PD_EN Set this bit to enable FPD CPU in sleep. (R/W)

RTC_CNTL_WIFI_PD_EN Set this bit to enable FPD wireless in sleep. (R/W)

RTC_CNTL_DG_WRAP_PD_EN Set this bit to enable FPD digital system in sleep. (R/W)
```