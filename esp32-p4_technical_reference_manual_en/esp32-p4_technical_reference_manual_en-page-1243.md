

```markdown
Chapter 20 System Registers (SYSREG)
GoBack

20.2.1.9 USB OTG 2.0 Control

ESP32-P4 features a USB 2.0 High-Speed On-The-Go peripheral (OTG_HS). To control it, use HP_SYSTEM_USBOTG20_CTRL_REG.

For details, please refer to Chapter 49 USB 2.0 High-Speed OTG.

20.2.1.10 CPU Control and Record

ESP32-P4 configures CPU debug features and stores its status information via the following system registers.

- HP_SYSTEM_CPU_CORESTALLED_ST_REG: records the core stalled status of CPU0 and CPU1.
- HP_SYSTEM_CORE_DEBUG_RUNSTALL_CONF_REG: write 1 to enable debug runstall feature between HP CPU and LP CPU.
- HP_SYSTEM_HP_CORE_DMACTIVE_LPCORE_REG: represents the dmacative value of LP CPU's debug module.

For details, please refer to Chapter 1 High-Performance CPU.

20.2.1.11 HP GPIO Hold Control

Each GPIO pin of ESP32-P4 has an individual hold function that is controlled by the following registers:

- HP_SYSTEM_GPIO_O_HOLD_CTRL0_REG: controls the hold signal of HP GPIO16 ~ HP GPIO47
- HP_SYSTEM_GPIO_O_HOLD_CTRL1_REG: controls the hold signal of GPIO48 ~ HP GPIO56
- HP_SYSTEM_GPIO_DED_HOLD_CTRL_REG: the lower 6 bits control the hold signal of flash pads, and the higher 20 bits control the hold signal of 16 line PSRAM pad

For details, please refer to Chapter 9 GPIO Matrix and IO MUX.

20.2.1.12 HP GPIO Output Control

Each GPIO pin of ESP32-P4 can be configured to directly output the desired value via the following registers (hysteresis):

- HP_SYSTEM_GPIO_O_HYS_CTRL0_REG: configures whether or not to enable the hysteresis feature of HP GPIO16 ~ HP GPIO47.
- HP_SYSTEM_GPIO_O_HYS_CTRL1_REG: configures whether or not to enable the hysteresis feature of HP GPIO48 ~ HP GPIO56.

For details, please refer to Section 9.10 in Chapter 9 GPIO Matrix and IO MUX.

20.2.1.13 Illegal Access and Unauthorized Access

ESP32-P4's buses return error response and record transfer address, transfer direction, and master id when illegal access and unauthorized access occur.

- Illegal access: access to unmapped address space
- Unauthorized access: access to mapped address space without permission

Such information will be logged in the following registers:
```