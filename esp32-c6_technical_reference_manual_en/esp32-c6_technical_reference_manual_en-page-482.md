

```markdown
Register 12.62. LP_AON_LPBUS_REG (0x0048)

LP_AON_FAST_MEM_MUX_SEL_STATUS LP_AON_FAST_MEM_MUX_SEL_UPDATE (reserved)
31    30    29    28
+----+----+----+----+
| 1 | 0 | 1 | 0 | ... | 0 |
+----+----+----+----+

LP_AON_FAST_MEM_MUX_SEL_STATUS Indicates whether the LP SRAM access mode switch has succeeded or not. (RO)

LP_AON_FAST_MEM_MUX_SEL_UPDATE Set this bit to 1 to switch the access mode. (WT)

LP_AON_FAST_MEM_MUX_SEL Configures the access mode to the LP SRAM.
0: Low-speed mode
1: High-speed mode
(R/W)
```

## 12.10.3 RTC Timer Registers

The addresses in this section are relative to the RTC Timer base address provided in Table 5.3-2 in Chapter 5 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 12.63. RTC_TIMER_TARO_LOW_REG (0x0000)

RTC_TIMER_MAIN_TIMER_TAR_LOWO

31
+------------------------------------------+
|                                         |
|    0x00000000                             | Reset
+------------------------------------------+

RTC_TIMER_MAIN_TIMER_TAR_LOWO Configures the low 32 bits of the target count value 0 (48 bits total) of the RTC timer. (R/W)
```