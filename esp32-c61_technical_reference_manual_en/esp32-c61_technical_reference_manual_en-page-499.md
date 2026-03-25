

```markdown
## 11.4.2.1 PMU Main State Machine

The PMU main state machine can receive sleep and wake-up signals, change the state of power and clock through the power controllers, thereby switching PMU states, and achieving a balance between performance and power consumption of the chip.

The PMU main state machine supports four PMU states and two transition states.

Each PMU state is controlled by different sleep and wake-up signals, supporting software customization of power and clocks. These four PMU states allow the software to expand power modes for various application scenarios. The four PMU states are:

*   HP_ACTIVE: PMU state where the circuits on the chip are powered up to a maximum, supporting the HP system and LP system operation.
*   HP_MODEM: PMU state where Modem (wireless MAC and baseband) can operate independently of the CPU.
*   HP_SLEEP: PMU state where the HP system is in sleep, supporting the operation of LP system.
*   LP_SLEEP: PMU state where HP system and LP peripherals are in sleep, while the always-on circuits remain operational.

Two transition states indicate that the PMU is waiting for the system to switch to a different power mode. For example, during the period of “waiting for the configured clock gating to take effect and the output clock to stabilize.”

*   HP_SWITCH: An intermediate state when the HP system switches between HP_ACTIVE, HP_MODEM, and HP_SLEEP. The hardware completes the control transition of various controllers in this state.
*   LP_SWITCH: An intermediate state when the LP system switches between HP_SLEEP and LP_SLEEP. The hardware completes the control transition of various controllers in this state.

**Note:**

Referring to [ESP32-C61 Datasheet > Functional Block Diagram](#) The division of HP and LP system is as follows:

*   LP system (peripherals): modules that are marked as “optional in Deep-sleep” in the Functional Block Diagram, such as LP IO.
*   LP system (always-on circuits): modules that are marked as “All modes” and “optional in Deep-sleep” in the Functional Block Diagram, such as PMU, RTC Watchdog Timer, Super Watchdog.
*   HP system: modules that are marked as “Active and Modem-sleep” in the Functional Block Diagram.

HP_ACTIVE, HP_MODEM, HP_SLEEP are the states of the HP system, while LP_SLEEP is the state of the LP system.

*   If a module belongs to the HP system, its power up/down can be configured in the HP_ACTIVE, HP_MODEM and HP_SLEEP states, but not in the LP_SLEEP state. In the LP_SLEEP state, it will reuse the HP_SLEEP state.
*   If a module belongs to the LP system, its power up/down can be configured in the HP_SLEEP and LP_SLEEP states. In the HP_ACTIVE and HP_MODEM states, it will reuse the HP_SLEEP configuration.

Take the CPU as an example: CPU belongs to the HP system, so it can be configured to power up/down in the
```