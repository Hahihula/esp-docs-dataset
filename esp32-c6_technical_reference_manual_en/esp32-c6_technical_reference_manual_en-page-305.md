

```markdown
- CPU Reset: resets CPU core. Once such reset is released, the instructions from the CPU reset vector will be executed.
- Core Reset: resets the whole digital system except LP system, including CPU, peripherals, Wi-Fi, Bluetooth® LE, and digital GPIOs.
- System Reset: resets the whole digital system, including LP system.
- Chip Reset: resets the whole chip.

• Software reset and hardware reset:
  - Software Reset: triggered via software by configuring the corresponding registers of CPU, see Chapter 12 Low-Power Management.
  - Hardware Reset: triggered directly by the hardware.
```

## 8.1.4 Functional Description

CPU will be reset immediately when any type of reset above occurs. Users can retrieve reset source codes by reading `RTC_CLKRST_RESET_CAUSE` after the reset is released. Table 8.1-1 lists possible reset sources and the types of reset they trigger.
```