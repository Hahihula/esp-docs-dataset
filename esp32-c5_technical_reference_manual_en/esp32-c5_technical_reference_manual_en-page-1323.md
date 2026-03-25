

```markdown
Chapter 36 Pulse Count Controller (PCNT)		[GoBack](#)
## 36.1 Features

A PCNT has the following features:

* Four independent pulse counters (units) that count from 1 to 65535
* Each unit consists of two independent channels sharing one pulse counter
* All channels have input pulse signals (e.g. `sig_ch0_un`) with their corresponding control signals (e.g. `ctrl_ch0_un`)
* Independently filter glitches of input pulse signals (`sig_ch0_un` and `sig_ch1_un`) and control signals (`ctrl_ch0_un` and `ctrl_ch1_un`) on each unit
* Each channel has the following parameters:
    1. Selection between counting on positive or negative edges of the input pulse signal
    2. Configuration to Increment, Decrement, or Disable counter mode for control signal’s high and low states
    3. Step count alert triggered by setting the upcount/downcount step threshold
    4. Clearing of the pulse count controller value by setting the clear register or sending a clear signal through GPIO input
    5. Generation and recording of a corresponding event signal for each counter mode, with the ability to report it to the interrupt task.
* Maximum frequency of input pulses: $\frac{f_{APB\_CLK}}{2}$
```