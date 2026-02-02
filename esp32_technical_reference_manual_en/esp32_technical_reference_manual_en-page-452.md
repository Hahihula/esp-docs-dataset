**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Body Text:**

To summarize, a few examples have been considered. In this table, the effect on the counter for a rising edge is shown for both a low and a high control signal, as well as various other configuration options. For clarity, a short description in brackets is added after the values. Note: x denotes 'do not care'.

**Table:**
| POS_MODE | LCTRL_MODE | HCTRL_MODE | sig1→h when ctrl=0 | sig1→h when ctrl=1 |
|----------|-------------|-------------|--------------------|---------------------|
| 1 (inc)  | O (-)       | O (-)       | Inc ctr            | Inc ctr             |
| 2 (dec)  | O (-)       | O (-)       | Dec ctr            | Dec ctr             |
| 0 (-)    | x           | x           | No action           | No action           |
| 1 (inc)  | O (-)       | 1 (inv)     | Inc ctr            | Dec ctr             |
| 1 (inc)  | 1 (inv)     | O (-)       | Inc ctr            | Dec ctr             |
| 2 (dec)  | O (-)       | 1 (inv)     | Dec ctr            | Inc ctr             |
| 1 (inc)  | O (-)       | 2 (dis)     | No action           | No action           |
| 1 (inc)  | 2 (dis)     | O (-)       | Inc ctr            | No action           |

This table is also valid for negative edges (sig h→l) on substituting NEG_MODE for POS_MODE.

Each pulse counter unit also features a filter on each of the four inputs, adding the option to ignore short glitches in the signals. If a PCNT_FILTER_EN_Un can be set to filter the four input signals of the unit. If this filter is enabled, any pulses shorter than REG_FILTER_THRES_Un number of APB_CLK clock cycles will be filtered out and will have no effect on the counter. With the filter disabled, in theory infinitely small glitches could possibly trigger pulse counter action. However, in practice the signal inputs are sampled on APB_CLK edges and even with the filter disabled, pulse widths lasting shorter than one APB_CLK cycle may be missed.

Apart from the input channels, software also has some control over the counter. In particular, the counter value can be frozen to the current value by configuring PCNT_CNT_PAUSE_Un. It can also be reset to 0 by configuring PCNT_PLUS_CNT_RST_Un.

**Subsection Title:**
23.2.3 Watchpoints

The pulse counters have five watchpoints that share one interrupt. Interrupt generation can be enabled or disabled for each individual watchpoint. The watchpoints are:

- Maximum count value: Triggered when PULSE_CNT >= PCNT_CNT_H_LIM_Un. Additionally, this will reset the counter to 0. PCNT_CNT_H_LIM_Un should be a positive number.
- Minimum count value: Triggered when PULSE_CNT <= PCNT_CNT_L_LIM_Un. Additionally, this will reset the counter to 0. PCNT_CNT_L_LIM_Un should be a negative number.
- Two threshold values: Triggered when PULSE_CNT = PCNT_THR_THRESH0_Un or PCNT_THR_THRESH1_Un.
- Zero: Triggered when PULSE_CNT = 0.

**Footer Information:**
Espressif Systems
452 ESP32 TRM (Version 5.6)
Submit Documentation Feedback