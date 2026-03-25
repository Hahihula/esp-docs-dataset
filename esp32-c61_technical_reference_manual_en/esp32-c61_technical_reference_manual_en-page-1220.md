

```markdown
The external reference voltage is accessed directly from the pad with an input range of 0 ~ (0.7 × VDDPST1) V, same as the internal reference voltage, requiring no additional configuration.

* Voltage comparison interrupt processing

The voltage comparison result, i.e., the COMP_OUT signal, can be either high or low. Whenever the output value changes, a corresponding interrupt signal is generated.
```

```markdown
## 34.5 Event Task Matrix Feature

The analog voltage comparator on ESP32-C61 supports the Event Task Matrix (ETM) function, which allows analog voltage comparator ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM events related to analog voltage comparator. For more information, please refer to Chapter 10 Event Task Matrix (ETM).

The analog voltage comparator can generate the following ETM events:

* GPIO_EVT_ZERO_DET_POS: Indicates that the COMP_OUT signal changes from low level to high level, i.e., the main voltage changes from below to above the reference voltage.
* GPIO_EVT_ZERO_DET_NEG: Indicates that the COMP_OUT signal changes from high level to low level, i.e., the main voltage changes from higher to lower than the reference voltage.

The analog voltage comparator does not support any ETM tasks.
```

```markdown
## 34.6 Interrupts

ESP32-C61’s analog voltage comparator can generate the GPIO_PAD_COMP_INT interrupt signal that will be sent to the Interrupt Matrix.

There are several internal interrupt sources from analog voltage comparator that can generate the above interrupt signal. The interrupt sources from analog voltage comparator are listed with their trigger conditions and the resulted interrupt signal(s) in Table 34.6-1.
```

```markdown
Table 34.6-1. Analog Voltage Comparator’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                 | Interrupt Signal         |
|---------------------------|-----------------------------------------------------------------------------------|--------------------------|
| GPIO_COMP_ALL_INT         | Any COMP_OUT signal transition occurs                                             | GPIO_PAD_COMP_INT       |
| GPIO_COMP_NEG_INT         | The COMP_OUT signal changes from high level to low level                          | GPIO_PAD_COMP_INT       |
| GPIO_COMP_POS_INT         | The COMP_OUT signal changes from low level to high level                          | GPIO_PAD_COMP_INT       |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 9 Interrupt Matrix > Section 9.2 Interrupt Terminology in ESP32-C61.
```