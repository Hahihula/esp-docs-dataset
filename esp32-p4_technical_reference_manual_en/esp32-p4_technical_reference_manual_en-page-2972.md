

```markdown
| Capacitive Touch Pin | Connected GPIO Pin |
|:----------------------|:--------------------|
| T1                    | GPIO2               |
| T2                    | GPIO3               |
| T3                    | GPIO4               |
| T4                    | GPIO5               |
| T5                    | GPIO6               |
| T6                    | GPIO7               |
| T7                    | GPIO8               |
| T8                    | GPIO9               |
| T9                    | GPIO10              |
| T10                   | GPIO11              |
| T11                   | GPIO12              |
| T12                   | GPIO13              |
| T13                   | GPIO14              |
| T14                   | GPIO15              |
```

## 60.3.3 Touch Sensor

The touch sensor charges and discharges the touch pin with a fixed current source, and each charge and discharge generates a pulse signal, the TOUCH_OUT signal. The touch sensor detects the capacitance change of the touch pin. If the touch pin is touched or approached by a finger, the touch pin's capacitance increases and the charging and discharging time is extended. By measuring the time required for charging and discharging the touch pin a fixed number of times, it can be inferred whether the touch pin has been touched or not.

Figure 60.3-2 illustrates the internal structure of the touch sensors. Each of the touch sensors has a set of input and output signals, some of which are connected to the Touch FSM (see Section 60.4.1). Table 60.3-2 shows the output signals of the touch sensor and their functions.
```