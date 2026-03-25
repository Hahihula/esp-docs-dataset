

```markdown
Figure 18.3-1. Architecture of Power Supply Detector


## 18.3.2 Brown-out Detector

The brown-out detector checks the voltage of pins VDD3P3 (PIN1,PIN2), VDDPST1, VDDPST2, VDDA_PMU, and VDD3P3 (PIN30,PIN31), about every 280 µs. When the voltage on these pins falls below a predefined threshold of 2.7 V (default setting), the detector activates a signal to power down the power-hungry RF circuits. This action provides additional time for the digital system to save and transfer important data. The brown-out detector consumes very little power and remains active as long as the chip is powered on.

`LP_ANA_BOD_MODEO_INT_RAW` indicates the detection result from the brown-out detector. By default, this register reads a value of 0. It changes to 1 when the voltage on the monitored pin falls below a predefined threshold.

When a brown-out signal is detected, the brown-out detector handles it in one of the following two modes (Mode 1 is the default):

*   Mode 0:
    -   Mode 0 is enabled by setting the `bod_mode0_en` (`LP_ANA_BOD_MODEO_INTR_ENA`) signal.
    -   The brown-out detector triggers an interrupt when the counter counts to the thresholds predefined in Int Comparer (`LP_ANA_BOD_MODEO_INTR_WAIT`). If `LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA` is set, flash suspend will be triggered; if `LP_ANA_BOD_MODEO_PD_RF_ENA` is set, the RF module will be powered down.
    -   The brown-out detector resets the chip based on the configuration of `bod_mode0_rst_sel` (`LP_ANA_BOD_MODEO_RESET_SEL`) when the brown-out counter counts to the thresholds predefined in Rst Comparer (`LP_ANA_BOD_MODEO_RESET_WAIT`). The reset is enabled by `bod_mode0_rst_en` (`LP_ANA_BOD_MODEO_RESET_ENA`).

*   Mode 1: Resets the system directly.

The brown-out reset workflow is illustrated in the diagram below.
```