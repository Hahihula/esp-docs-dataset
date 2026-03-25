

```markdown
Chapter 13 Low-Power Management

GoBack

13.4.2.1 PMU Main State Machine

The PMU main state machine receives sleep and wake-up signals, changes the state of power and clock through the power controllers, thereby switching PMU states, and achieving a balance between performance and power consumption of the chip.

The PMU main state machine supports four PMU states, each controlled by different sleep and wake-up signals, supporting software customization of power and clocks. These PMU states allow the software to expand power modes for various application scenarios. The four PMU states are:

*   HP_ACTIVE: The circuits on the chip are powered up to a maximum, supporting the HP system and LP system operation.
*   HP_MODEM: Modem (wireless MAC and baseband) can operate independently of the CPU.
*   HP_SLEEP: The HP system is in sleep, supporting LP peripherals operation.
*   LP_SLEEP: The HP system and LP peripherals are in sleep, while the always-on circuits remain operational.

Note:

The division of HP and LP system is as follows:

*   LP system (peripherals): LP RISC-V 32-bit Microprocessor, LP GPIO, LP UART, LP I2C
*   LP system (always-on circuits): LP Memory (LP SRAM), PMU, RTC Watchdog Timer, RTC Super Watchdog Timer, RTC Timer, eFuse Controller, Power Glitch Detector
*   HP system: All peripherals (including Modem) except those belonging to the LP system.

For more details, please refer to ESP32-C5 Datasheet > Functional Block Diagram.

HP_ACTIVE, HP_MODEM, HP_SLEEP are the states of the HP system, while LP_SLEEP is the state of the LP system.

*   If a module belongs to the HP system, its power up/down is configured in the HP_ACTIVE/HP_MODEM/HP_SLEEP states, but not in the LP_SLEEP state. It reuses the HP_SLEEP configuration in the LP_SLEEP state.
*   If a module belongs to the LP system, its power up/down is configured in the LP_SLEEP state and reuses the HP_SLEEP configuration in the HP_ACTIVE/HP_MODEM/HP_SLEEP states.

Take the HP CPU as an example. Since the HP CPU belongs to the HP system, it can be powered up or down in HP_ACTIVE/HP_MODEM/HP_SLEEP states through the following registers and reuse the HP_SLEEP configuration in LP_SLEEP.

*   HP_ACTIVE: PMU_HP_ACTIVE_PD_HP_CPU_PD_EN
*   HP_MODEM: PMU_HP_MODEM_PD_HP_CPU_PD_EN
*   HP_SLEEP: PMU_HP_SLEEP_PD_HP_CPU_PD_EN

Similarly, users can define other power domains’ power up and down in different PMU states. For the configuration registers, please refer to Section 13.9.
```