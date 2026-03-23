

```markdown
| Power Modes | LP always-on | LP PD peripherals | Peripherals | Modem | CPU | RC_FAST_CLK | XTAL_CLK | PLL | RF circuit |
|-------------|--------------|---------------------|-----------|-------|-----|------------|----------|-----|-------------|
| Active      | ON           | ON                  | ON        | ON    | ON  | ON         | ON       | ON  | ON          |
| Modem-sleep | ON           | ON                  | ON        | OFF   | ON  | ON         | ON       | ON/OFF | OFF         |
| Light-sleep0| ON           | ON                  | ON        | ON/OFF| OFF | ON         | ON/OFF   | ON/OFF | ON/OFF      |
| Light-sleep1| ON           | ON/OFF              | ON/OFF    | ON/OFF| OFF | ON/OFF     | ON/OFF   | ON/OFF | ON/OFF      |
| Deep-sleep  | ON           | OFF                 | OFF       | OFF   | OFF | OFF        | OFF      | OFF  | OFF         |

Note:
1. For power consumption data, please refer to ESP32-C6 Datasheet > Section Current Consumption.
2. For supported wake-up sources, please refer to Table 12.4-1.
```

## 12.6 RTC Boot

In Deep-sleep mode, both the ROM and RAM of the chip are powered down, so the time required for SPI Boot (copying data from flash) upon waking up is long. Therefore, compared to Light-sleep and Modem-sleep modes, the wake-up from Deep-sleep mode takes longer time. However, in Deep-sleep mode, the 16 KB SRAM can remain powered up. Therefore, users can put small-sized code (i.e., less than 8 KB "deep sleep wake stubs") into the 16 KB SRAM to avoid the delay caused by SPI boot, thus speeding up the chip wake-up process.

To enable RTC boot, follow the steps below:

1. Set `LP_AON_CORE0_STAT_VECTOR_SEL` to 1 to start up the chip from the RTC fast memory.
2. Calculate CRC for the RTC fast memory and save the result in `LP_AON_STORE7_REG`.
3. Set `LP_AON_STORE6_REG` to the entry address of the RTC fast memory.
4. Configure sleep mode for the chip.
5. When the CPU is powered up, it begins unpacking the ROM and performing initialization. Then, recalculate the CRC code of the RTC fast memory. If it matches the result stored in `LP_AON_STORE7_REG`, the CPU will jump to the entry address of the RTC fast memory.

The boot flow after the chip’s wake-up is shown in Figure 12.6-1.
```