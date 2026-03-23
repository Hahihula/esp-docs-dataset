
```markdown
# 15.5 Register Summary

The addresses in this section are relative to RTC_WDT base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| configuration register |  |  |  |
| RTC_WDT_CONFIG0_REG | Configure the RWDT operation | 0x0000 | R/W |
| RTC_WDT_CONFIG1_REG | Configure the RWDT timeout time of stage0 | 0x0004 | R/W |
| RTC_WDT_CONFIG2_REG | Configure the RWDT timeout time of stage1 | 0x0008 | R/W |
| RTC_WDT_CONFIG3_REG | Configure the RWDT timeout time of stage2 | 0x000C | R/W |
| RTC_WDT_CONFIG4_REG | Configure the RWDT timeout time of stage3 | 0x0010 | R/W |
| RTC_WDT_FEED_REG | Configure the feed function of RWDT | 0x0014 | WT |
| RTC_WDT_WPROTECT_REG | Configure the lock function of RWDT | 0x0018 | R/W |
| RTC_WDT_SWD_CONFIG_REG | Configure the SWD operation | 0x001C | varies |
| RTC_WDT_SWD_WPROTECT_REG | Configure the lock function of SWD | 0x0020 | R/W |
| RTC_WDT_INT_RAW_REG | The interrupt raw register of WDT | 0x0024 | R/WTC/SS |
| RTC_WDT_INT_ST_REG | The interrupt status register of WDT | 0x0028 | RO |
| RTC_WDT_INT_ENA_REG | The interrupt enable register of WDT | 0x002C | R/W |
| RTC_WDT_INT_CLR_REG | The interrupt clear register of WDT | 0x0030 | WT |
| RTC_WDT_DATE_REG | Version control register | 0x03FC | R/W |

# 15.6 Registers

MWDT registers are part of the timer submodule and are described in Section 14.5 Register Summary in Chapter 14 Timer Group (TIMG).

The addresses of RWDT and SWD registers in this section are relative to RTC_WDT base address provided in Table 5.3-2 in Chapter 5 System and Memory.
```