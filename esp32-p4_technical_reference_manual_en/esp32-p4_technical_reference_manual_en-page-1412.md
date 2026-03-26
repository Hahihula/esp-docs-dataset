

```markdown
- 1: 2.3 V
- 2: 2.4 V
- 3: 2.5 V
- 4: 2.6 V
- 5: 2.7 V
- 6: 2.8 V
- 7: 2.9 V

* Voltage-monitoring filter

A dedicated glitch filter is used to process the detection results of VDD_BAT, as shown in the figure below.

![Figure 23.4-1. Structure of Brown-out Detector](image_path_if_available)

Figure 23.4-1. Structure of Brown-out Detector

- vdd_cnt: the value of the brown-out counter.
- bod_source: the monitored source, which is VDD_BAT in the figure.
- vdd_undervoltage_flag: the under-voltage flag.

- Stage 0 ~ 1: When bod_source is 1, it indicates the voltage is normal, and the brown-out counter (vdd_cnt) remains 0.

- Stage 1 ~ 2: When bod_source is 0, it indicates under-voltage happens, and the brown-out counter will start to count. When the counter value reaches the corresponding threshold, vdd_undervoltage_flag will be set to 1, and the interrupt is generated.
```