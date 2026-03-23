

```markdown
Chapter 6 Reset and Clock                          GoBack

- Core Reset: Resets the whole digital system except RTC, including CPU, peripherals, Wi-Fi, Bluetooth® LE, and digital GPIOs.
- System Reset: Resets the whole digital system, including RTC.
- Chip Reset: Resets the whole chip.

• Support software reset and hardware reset:
  - Software Reset: the CPU can trigger a software reset by configuring the corresponding registers, see Chapter 9 Low-power Management.
  - Hardware Reset: Hardware reset is directly triggered by the circuit.

Note:
If CPU is reset, PMS registers will be reset, too.

6.1.4 Functional Description

CPU will be reset immediately when any of the reset above occurs. Users can get reset source codes by reading register RTC_CNTL_RESET_CAUSE_PROCPU after the reset is released.

Table 6.1-1 lists possible reset sources and the types of reset they trigger.
```