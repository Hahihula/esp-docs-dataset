

```markdown
## Register 12.60. LP_AON_SYS_CFG_REG (0x0034)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 30  | LP_AON_HPSYS_SW_RESET        |
| 29  | LP_AON_FORCE_DOWNLOAD_BOOT   |

LP_AON_FORCE_DOWNLOAD_BOOT Configures whether to trigger a CPU reset and switch the chip boot mode.
- O: No effect.
- 1: If `EFUSE_DIS_FORCE_DOWNLOAD` is 0, software can force switch the chip from SPI Boot mode to Joint Download Boot mode and trigger a CPU reset. (R/W)

LP_AON_HPSYS_SW_RESET Configures System Reset.
- O: No effect
- 1: Enable reset (WT)


## Register 12.61. LP_AON_CPUCOREO_CFG_REG (0x0038)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | reserved                                 |
| 30  | LP_AON_CPU_COREO_SW_RESET                |
| 29  | LP_AON_COREO_STAT_VECTOR_SEL             |
| 28  | (reserved)                               |

LP_AON_CPU_COREO_SW_RESET Configures CPU Reset.
- O: No effect
- 1: Enable reset (WT)

LP_AON_COREO_STAT_VECTOR_SEL Configures whether to start up the CPU from the RTC fast memory.
- O: Do not start up from the RTC fast memory.
- 1: Start up from the RTC fast memory. (R/W)
```