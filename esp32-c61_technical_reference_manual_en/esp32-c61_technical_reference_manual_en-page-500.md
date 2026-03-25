

```markdown
HP_ACTIVE, HP_MODEM and HP_SLEEP states through the following registers and reuses the HP_SLEEP configuration in LP_SLEEP.

*   `HP_ACTIVE`: PMU_HP_ACTIVE_PD_HP_CPU_PD_EN
*   `HP_MODEM`: PMU_HP_MODEM_PD_HP_CPU_PD_EN
*   `HP_SLEEP`: PMU_HP_SLEEP_PD_HP_CPU_PD_EN

Similarly, users can define other power domains' power up and down in different PMU states. For specific registers, please refer to Section 11.8.

Note:

In the following text, all such registers will be collectively referred to as **PMU_PMUSTATE_PD_POWERDOMAIN_PD_EN**, where, unless specified otherwise:

*   `PMUSTATE` represents HP_ACTIVE, HP_MODEM, HP_SLEEP and LP_SLEEP.
*   `POWERDOMAIN` represents TOP, HP_AON, HP_CPU, HP_WIFI, HP_MEM and LP_PERI.

All such registers are linked to a representative of the same type for reference. For example,
**PMU_PMUSTATE_PD_POWERDOMAIN_PD_EN** will be linked to **PMU_HP_ACTIVE_PD_TOP_PD_EN**.
```

```markdown
11.4.2.2 Sleep/Wake-up Controller

The sleep/wake-up controller is responsible for initiating sleep and wake-up requests to the PMU main state machine. ESP32-C61 supports multiple wake-up sources to wake the CPU from different power modes that can be enabled through **PMU_WAKEUP_ENA**.
```