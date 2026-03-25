

```markdown
| Power Modes | LP always-on | LP PD peripherals | Peripherals + ROM | Power Domain Modem | CPU | RC_FAST_CLK | XTAL_CLK | PLL | RF circuit |
|-------------|--------------|-------------------|------------------|--------------------|-----|------------|----------|-----|-------------|
| Active      | ON           | ON                | ON               | ON                 | ON  | ON         | ON       | ON  | ON          |
| Modem-sleep | ON           | ON                | ON               | ON                 | ON  | ON         | ON       | ON/OFF | OFF         |
| Light-sleep0| ON           | ON                | ON               | ON/OFF             | OFF | ON         | ON/OFF   | ON/OFF | ON/OFF      |
| Light-sleep1| ON           | ON/OFF            | ON/OFF           | ON/OFF             | OFF | ON/OFF     | ON/OFF   | ON/OFF | ON/OFF      |
| Deep-sleep  | ON           | OFF               | OFF              | OFF                | OFF | OFF        | OFF      | OFF  | OFF         |

Note:
1. For power consumption data, please refer to [ESP32-C5 Datasheet > Section Current Consumption](#).
2. For supported wake-up sources, please refer to Table 13.4-1.
```

### 13.6 RTC Boot

In Deep-sleep mode, both the ROM and RAM of the chip are powered down, so the time required for SPI Boot (copying data from flash) upon waking up is long. Therefore, compared to Light-sleep and Modem-sleep modes, the wake-up from Deep-sleep mode takes longer time. However, in Deep-sleep mode, the 16 KB SRAM can remain powered up. Therefore, users can put small-sized code (i.e., "deep sleep wake stubs") into the 16 KB SRAM to avoid the delay caused by SPI boot, thus speeding up the chip wake-up process.

To enable RTC boot, follow the steps below:

1. Set `LP_AON_COREO_STAT_VECTOR_SEL` to 0 to start up the chip from the LP SRAM.
```