

```markdown
2. Calculate CRC for of "deep sleep wakeup stubs" in the LP SRAM and save the result in `LP_AON_STORE7_REG`.
3. Set `LP_AON_STORE6_REG` to the entry address of the "deep sleep wakeup stubs" in LP SRAM.
4. Configure sleep mode for the chip.
5. When the CPU is powered up, it begins unpacking the ROM and performing partial initialization. Then, the CPU recalculates the CRC code of the RTC fast memory. If the result matches what is stored in `LP_AON_STORE7_REG`, the CPU jumps to the "deep sleep wakeup stubs". If the CRC does not match, the CPU directly enters the SPI boot process.

Figure 13.6-1 shows the boot flow after the chip's wake-up.
```

![Figure 13.6-1. ESP32-C5 Boot Flow](image)

```markdown
## 13.7 Event Task Matrix Feature

The low-power management system on ESP32-C5 supports the Event Task Matrix (ETM) function, which allows the low-power management system's ETM tasks to be triggered by any peripherals' ETM events, or the low-power management system's ETM events to trigger any peripherals' ETM tasks. This section introduces
```