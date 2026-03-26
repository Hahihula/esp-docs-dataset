

```markdown
Figure 63.3-1. Analog Voltage Comparator Architecture


As shown in the figure above, the analog voltage comparator consists of:

*   Two pad interfaces:
    -   PAD1: Main voltage interface
    -   PADO: External reference voltage interface
*   VREF: Internal reference voltage interface
*   mode_control: Register-controlled switch for selecting the reference voltage source
*   COMP_OUT: Comparator voltage comparison result, which is an on-chip internal signal that cannot be directly accessed externally

    -   If the main voltage is higher than the reference voltage, the COMP_OUT signal is high.
    -   If the main voltage is lower than the reference voltage, the COMP_OUT signal is low.


## 63.4 Functional Description

The analog voltage comparator has the following functions:

*   Voltage comparison

    The analog voltage comparator relies on a specialized pads that support voltage comparison. For more information about general-purpose pads, please refer to Chapter 9 GPIO Matrix and IO MUX. Table below shows the mapping between the PAD of analog voltage comparator `0` and GPIO pins.

Table 63.4-1. Mapping Between PAD and GPIO

| Analog Voltage Comparator | PADO   | PAD1   |
|----------------------------|--------|--------|
| Analog voltage comparator 0 | GPIO51 | GPIO52 |
| Analog voltage comparator 1 | GPIO53 | GPIO54 |

The comparison mode and reference voltage are configurable. For detailed configuration procedures, see Section 63.7 Programming Procedures.

The voltage comparison results are output as the COMP_OUT signal.
```