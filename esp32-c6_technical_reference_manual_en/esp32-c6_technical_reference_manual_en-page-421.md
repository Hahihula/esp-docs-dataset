

```markdown
Chapter 12 Low-Power Management

The PMU main state machine supports four PMU states, each controlled by different sleep and wake-up signals, supporting software customization of power and clocks. These four PMU states allow the software to expand power modes for various application scenarios. The four PMU states are:

*   HP_ACTIVE: PMU state where the circuits on the chip are powered up to a maximum, supporting the HP system and LP system operation.
*   HP_MODEM: PMU state where Modem (wireless MAC and baseband) can operate independently of the CPU.
*   HP_SLEEP: PMU state where the HP system is in sleep, supporting LP peripherals operation.
*   LP_SLEEP: PMU state where HP system and LP peripherals are in sleep, while the always-on circuits remain operational.

Note:
The division of HP and LP system is as follows:

*   LP system (peripherals): LP RISC-V 32-bit Microprocessor, LP Memory, LP IO, LP UART, LP I2C
*   LP system (always-on circuits): PMU, RTC Watchdog Timer, Super Watchdog
*   HP system: This includes all peripherals (including Modem) except those belonging to LP system.

For more details, please refer to ESP32-C6 Datasheet > Functional Block Diagram.
```

```markdown
HP_ACTIVE, HP_MODEM, HP_SLEEP are the states of the HP system, while LP_SLEEP is the state of the LP system.

*   If a module belongs to the HP system, its power up/down can be configured in the HP_ACTIVE/HP_MODEM/HP_SLEEP states, but not in the LP_SLEEP state. It will reuse the HP_SLEEP state in the LP_SLEEP state.
*   If a module belongs to the LP system, its power up/down can be configured in the LP_SLEEP state and will reuse the HP_SLEEP configuration in the HP_ACTIVE/HP_MODEM/HP_SLEEP states.

Take the HP CPU as an example. The HP CPU belongs to the HP system, so it can be configured to power up/down in the HP_ACTIVE/HP_MODEM/HP_SLEEP states through the following registers and reuse the HP_SLEEP configuration in LP_SLEEP.
*   HP_ACTIVE: PMU_HP_ACTIVE_PD_HP_CPU_PD_EN
*   HP_MODEM: PMU_HP_MODEM_PD_HP_CPU_PD_EN
*   HP_SLEEP: PMU_HP_SLEEP_PD_HP_CPU_PD_EN

Similarly, users can define other power domains' power up and down in different PMU states. For specific registers, please refer to Section 12.9.

Note:
In the following text, all such registers will be collectively referred to as PMU_n1_PD_POWERDOMAIN_PD_EN, where n1 represents the four PMU states.
```

```markdown
Once the configuration is done, PMU will use various controllers to make these configurations effective, as

Espressif Systems 421 ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```