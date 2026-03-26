

```markdown
2. If using LDO mode, configure output voltage: configure PMU_ANA_0PxADREF_y and PMU_ANA_0PxAMUL_y to satisfy VOUT = MUL × VREF.
3. Configure waiting counter: set stage 1 (TARGET0) to the desired over-current protection duration and stage 2 (TARGET1) to the voltage stabilization waiting time (see Table 14.4-6).
4. Enable over-current protection before power-up: set PMU_ANA_0PxA_EN_CUR_LIM_y=1 (see Table 14.4-5).
5. Enable the regulator: set PMU_0PxAXPD_y=1 (see Table 14.4-4), then wait for the stage 1 timeout interrupt (e.g., V03 uses PMU_0P2A_CNTARGET0_REACH0_INT, V04 uses PMU_0P2A_CNTARGET0_REACH1_INT).
6. After stage 1 interrupt, disable over-current protection: clear PMU_ANA_0PxA_EN_CUR_LIM_y. If a voltage stabilization waiting time is required, wait for the stage 2 timeout interrupt (....CNT_TARGET1_REACH....INT).

## 14.5 Power Modes

ESP32-P4 has three configurable PMU states. Based on the PMU states, the chip has defined five power modes for common application scenarios, as shown in Table 14.5-1.

**Table 14.5-1. Preset Power Modes**

| Power Modes | LP always-on | LP PD peripherals | HP_CPU | TOP | HPCNNT | RC_FAST_CLK | XTAL_CLK | PLL |
|-------------|--------------|-------------------|--------|-----|--------|-------------|----------|-----|
| Active      | ON           | ON                | ON     | ON  | ON     | ON          | ON       | ON  |
| Light-sleep0| ON           | ON                | OFF    | ON  | ON     | ON          | ON       | ON  |
| Light-sleep1| ON           | ON                | OFF    | ON  | ON     | ON/OFF      | ON/OFF   | ON/OFF |
| Light-sleep2| ON           | ON/OFF            | OFF    | OFF | ON/OFF | ON/OFF      | ON/OFF   | ON/OFF |
| Deep-sleep  | ON           | OFF               | OFF    | OFF | OFF    | OFF         | OFF      | OFF |

**Note:**
1. For power consumption data, please refer to ESP32-P4 Datasheet.
2. For supported wake-up sources, please refer to Table 14.4-1.

## 14.6 Event Task Matrix Feature

The low-power management system on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows the low-power management system's ETM tasks to be triggered by any peripherals' ETM events, or the low-power management system's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to the low-power management system. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

The low-power management system can receive the following ETM tasks:
```