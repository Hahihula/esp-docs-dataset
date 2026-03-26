

```markdown
## 23.3 Architectural Overview

Figure 23.3-1. Brown-out Detector Overview

* Source selection for detection: The brown-out detector can select which power source to monitor by configuring LP_ANA_BOD_SOURCE_ENA. RTC_VGOOD_VBAT indicates the detection result of VDD_BAT, and RTC_VGOOD_VDDA indicates the detection result of VDD_ANA.
* Brown-out detector (Brown Out): An analog circuit designed to monitor the voltage of power pins and generate brown-out signals. It compares the voltage with the predefined threshold. When the voltage falls below this threshold, the detector outputs brown-out signals.
* Brown-out counter (brownout cnt): A counter used for filtering voltage noise on the detected power pins. When the brown-out signal is received, the counter starts counting based on the clock source LP_DYN_FAST_CLK. If the brown-out signal ceases during the counting process, the counter resets to 0. This counter can be cleared by configuring LP_ANA_BOD_MODE0_CNT_CLR.
* Interrupt comparator (cmp0): The comparator generates interrupts by comparing the counter value with the threshold. When the counter value exceeds the threshold, the comparator generates the interrupt signal bod_modeO_int. If LP_ANA_BOD_MODE0_CLOSE_FLASH_ENA is enabled, bod_mode0_close_flash will be triggered, causing flash to enter the SUSPEND state.
* Reset comparator (cmp1): The comparator triggers reset signals by comparing the counter value with the threshold. When the counter value exceeds the threshold, the comparator triggers reset signals.

## 23.4 Functional Description

### Monitored sources
- VDD_ANA: Power pin for the analog circuit, supporting both Mode 0 and Mode 1.
- VDD_BAT: Power pin connected to the battery, supporting both Mode 0 and Mode 1. In addition, it supports two configurable voltage thresholds:
    * VBAT_BOD: Used for brown-out detection of VDD_BAT
```