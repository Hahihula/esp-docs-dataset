

```markdown
Chapter 7 Reset and Clock

GoBack

71.3 Features

- Four reset types:
    - CPU Reset: resets CPU core. Once such a reset is released, the instructions from the CPU reset vector (0x40000000) will be executed.
    - Core Reset: resets the whole digital system except LP system, including CPU, peripherals, digital GPIOs, Bluetooth® LE, and 802.15.4.
    - System Reset: resets the whole digital system, including LP system.
    - Chip Reset: resets the whole chip.

- Software reset and hardware reset:
    - Software Reset: triggered via software by configuring the corresponding registers of CPU, see Chapter 11 Low-Power Management.
    - Hardware Reset: triggered directly by the hardware.

71.4 Functional Description

CPU will be reset immediately when any type of reset above occurs. Users can retrieve reset source codes by reading RTC_CLKRST_RESET_CAUSE after the reset is released. Table 71-1 lists possible reset sources and the types of reset they trigger.
```