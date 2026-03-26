

```markdown
* HP CPU1 is at reset by default after chip power-up, and needs to be manually released from reset by writing 0 to `HP_SYS_CLKRST_RST_EN_CORE1_GLOBAL`. Once released from reset, HP CPU1 will start execution from CPU Reset Vector (0x30100000).
* LP CPU is at reset after chip power-up, and needs to be manually released from reset by configuring the power management unit (PMU). Once released from reset, LP CPU will start execution from `LP_SYSTEM_LP_CPU_BOOT_ADDR` (0x50100000 by default). For details, see Chapter 14 Low-Power Management.

- Core Reset: resets the whole digital system except for LP AON. HP core and LP core can be reset independently: HP Core Reset resets HP CPU0, HP CPU1, HP peripherals, HP GPIO, etc., and LP Core Reset resets LP CPU and LP peripherals.
- System Reset: resets the whole digital system, including the LP system.
- Chip Reset: resets the whole chip.

* Software reset and hardware reset:
  - Software Reset: triggered via software by configuring the corresponding registers of CPU, see Chapter 14 Low-Power Management.
  - Hardware Reset: triggered directly by the hardware.

## 10.1.4 Functional Description

CPU will be reset immediately when any type of reset above occurs. After the reset is released, users can retrieve reset source codes by reading the following fields:

* HP CPU0: `LP_CLKRST_HPCORE0_RESET_CAUSE`
* HP CPU1: `LP_CLKRST_HPCORE1_RESET_CAUSE`
* LP CPU: `LP_CLKRST_LPCORE_RESET_CAUSE`

Table 10.1-1 and Table 10.1-2 list possible reset sources and the types of reset they trigger.

**Table 10.1-1. HP CPU Reset Source**

| Code | Source                  | Reset Type         | Note                                                                 |
|------|-------------------------|--------------------|-----------------------------------------------------------------------|
| 0x01 | Chip reset¹             | Chip Reset         | —                                                                     |
| 0x03 | Software system reset   | HP Core Reset      | Triggered by configuring `LP_SYSTEM_SYS_SW_RST`                      |
| 0x05 | PMU core reset          | HP Core Reset      | See Chapter 14 Low-Power Management                                   |
| 0x07 | MWDT core reset²        | HP Core Reset      | See Chapter 17 Watchdog Timers (WDT)                                  |
| 0x09 | RWDT core reset         | HP Core Reset      | See Chapter 17 Watchdog Timers (WDT)                                  |
| 0x0B | MWDT CPU reset          | HP CPU0/1 Reset    | See Chapter 17 Watchdog Timers (WDT) by configuring                   |
|      |                         |                    | Triggered                                                             |
|      |                         |                    | `LP_CLKRST_HPCORE0_SW_RESET` or                                    |
|      |                         |                    | `LP_CLKRST_HPCORE1_SW_RESET`                                        |
| 0xOC | Software CPU reset      | HP CPU0/1 Reset    | See Chapter 17 Watchdog Timers (WDT)                                  |
| 0xOD | RWDT CPU reset          | HP CPU0/1 Reset    | See Chapter 17 Watchdog Timers (WDT)                                  |

Cont'd on next page
```