

```markdown
Note:

The division of the HP and LP systems is as follows:

*   LP system (peripherals): LP RISC-V 32-bit Microprocessor, LP GPIO, LP UART, LP I2C, LP I2S, touch sensor, temperature sensor, LP ADC, LP SPI
*   LP system (always-on circuits): PMU, RTC Watchdog Timer, Super Watchdog
*   HP system: All peripherals except those belonging to the LP system.

For more details, please refer to ESP32-P4 Datasheet > Functional Block Diagram.
```

HP_ACTIVE is the operating state of the HP system, HP_SLEEP is the sleep state of the HP system, LP_SLEEP is the sleep state of the LP system. The operating state of the LP system reuses the HP_SLEEP state and is therefore also referred to as HP_SLEEP.

*   If a module belongs to the HP system, its power up/down can be configured in the HP_ACTIVE/HP_SLEEP states. It reuses the HP_SLEEP state in the LP_SLEEP state.
*   If a module belongs to the LP system, its power up/down can be configured in the HP_SLEEP/LP_SLEEP state. It reuses the HP_SLEEP state in the HP_ACTIVE state.

Take the HP CPU as an example. The HP CPU belongs to the HP system, so it can be configured to power up/down in the HP_ACTIVE/HP_SLEEP states through the following registers and reuse the HP_SLEEP configurations in LP_SLEEP.

*   HP_ACTIVE: PMU_HP_ACTIVE_PD_HP_CPU_PD_EN
*   HP_SLEEP: PMU_HP_SLEEP_PD_HP_CPU_PD_EN

Similarly, users can configure the power up and down for other power domains in different PMU states. For the configuration registers, please refer to Section 14.8.

Note:

In the following text, all such configuration registers are collectively referred to as PMU_n1_PD_POWERDOMAIN_PD_EN, where n1 represents the three PMU states.

Once the configuration is done, the PMU uses various controllers to make these configurations effective, as described in the following sections.

### 14.4.2.2 Sleep/Wake-up Controller

The sleep/wake-up controller initiates sleep and wake-up requests to the PMU main state machine. ESP32-P4 supports multiple wake-up sources to wake the CPU from different power modes. Table 14.4-1 lists all the wake-up sources.

All the wake-up sources in Table 14.4-1 can wake up both the HP CPU and the LP CPU. Users can configure PMU_WAKEUP_ENA to set the target to the HP CPU, and configure PMU_LP_CPU_WAKEUP_EN to set the target to the LP CPU. Configuring both registers simultaneously can wake up both the HP CPU and the LP CPU.
```