---
original_file_path: api-reference/system/inc/power_management_esp32c5.rst
---

::: {.flat-table widths="1 3 3"}
- - Max CPU Frequency Set
  - Lock Acquisition
  - CPU and APB Frequencies
- - `2`{.interpreted-text role="rspan"} 240
  - `ESP_PM_CPU_FREQ_MAX` acquired
  - \- CPU: 240 MHz - APB: 80 MHz
- - `ESP_PM_APB_FREQ_MAX` acquired, `ESP_PM_CPU_FREQ_MAX` not acquired
  - \- CPU: 80 MHz - APB: 80 MHz
- - None
  - Min values for both frequencies set with `esp_pm_configure`{.interpreted-text role="cpp:func"}
- - `1`{.interpreted-text role="rspan"} 80
  - Any of `ESP_PM_CPU_FREQ_MAX` or `ESP_PM_APB_FREQ_MAX` acquired
  - \- CPU: 80 MHz - APB: 80 MHz
- - None
  - Min values for both frequencies set with `esp_pm_configure`{.interpreted-text role="cpp:func"}
:::
