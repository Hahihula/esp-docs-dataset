

```markdown
- Each channel has the following parameters:
    1. Selection between counting on rising or falling edges of the input pulse signal
    2. Configuration to Increment, Decrement, or Disable counter mode for control signal's high and low states
        - Maximum frequency of pulses: $\frac{f_{APB\_CLK}}{2}$
```

## 48.3 Architectural Overview

Each unit of PCNT includes two channels (ch0 and ch1) and the functionality of the two channels is identical. The remainder of the chapter will take channel 0 (ch0) as example and $n$ denotes the number of a unit from 0 ~ 3. Each channel of PCNT has two input signals:

1. One input pulse signal (e.g., sig_ch0_un, the input pulse signal for ch0 of unit $n$ ch0)
2. One control signal (e.g., ctrl_ch0_un, the control signal for ch0 of unit $n$ ch0)

![Figure 48.3-1. PCNT Architectural Overview](image_path_if_available)

**Figure 48.3-1 shows PCNT’s architecture. As stated above, `ctrl_ch0_un` is the control signal for ch0 of unit $n$. Its high and low states can be assigned in different counter modes and used for pulse counting of the channel’s input pulse signal `sig_ch0_un` on falling or rising edges.**
```