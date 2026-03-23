

# 11.5 Registers

The addresses in this section are relative to Timer Group base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 11.1. TIMG_TOCONFIG_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | 30          | 29         | ... | 0   |
| O   | 1           | 1          |     | Reset |

- **TIMG_TO_USE_XTAL** 1: Use XTAL_CLK as the source clock of timer group. 0: Use APB_CLK as the source clock of timer group. (R/W)
- **TIMG_TO_ALARM_EN** When set, the alarm is enabled. This bit is automatically cleared once an alarm occurs. (R/W/SC)
- **TIMG_TO_DIVIDER_RST** When set, Timer 0's clock divider counter will be reset. (WT)
- **TIMG_TO_DIVIDER** Timer 0 clock (TO_clk) prescaler value. (R/W)
- **TIMG_TO_AUTORELOAD** When set, Timer 0 auto-reload at alarm is enabled. (R/W)
- **TIMG_TO_INCREASE** When set, the Timer 0 time-base counter will increment every clock tick. When cleared, the Timer 0 time-base counter will decrement. (R/W)
- **TIMG_TO_EN** When set, the Timer 0 time-base counter is enabled. (R/W)

## Register 11.2. TIMG_TOLO_REG (0x0004)

| Bit | Description |
|-----|-------------|
| 31  | ...         | 0          |
|     |             |            |

- **TIMG_TO_LO** After writing to TIMG_TOUPDATE_REG, the low 32 bits of the time-base counter of Timer 0 can be read here. (RO)