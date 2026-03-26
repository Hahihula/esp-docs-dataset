

```markdown
Chapter 14 Low-Power Management

Figure 14.4-2. PMU Workflow

The following sections describe the main parts of PMU.

14.4.2.1 PMU Main State Machine

The PMU main state machine receives sleep and wake-up signals, changes the state of power and clock through the power controllers, thereby switching PMU states, and achieving a balance between performance and power consumption of the chip.

The PMU main state machine supports three PMU states, each controlled by different sleep and wake-up signals, supporting software customization of power and clocks. These PMU states allow the software to expand power modes for various application scenarios. The three PMU states are:

*   **HP_ACTIVE**: The circuits on the chip are powered up to a maximum, supporting the HP system and LP system operation.
*   **HP_SLEEP**: The HP system is in sleep, supporting LP peripherals operation.
*   **LP_SLEEP**: The HP system and LP peripherals are in sleep, while the always-ons circuits remain operational.

Espressif Systems
983
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```