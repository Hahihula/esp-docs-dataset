---
original_file_path: api-reference/system/inc/power_management_esp32h2.rst
---

::: {.flat-table widths="1 3 3"}
- - Max CPU Frequency Set
  - Lock Acquisition
  - CPU and APB Frequencies
- - `2`{.interpreted-text role="rspan"} 96
  - `ESP_PM_CPU_FREQ_MAX` acquired
  - \- CPU: 96 MHz - APB: 32 MHz
- - `ESP_PM_APB_FREQ_MAX` acquired, `ESP_PM_CPU_FREQ_MAX` not acquired
  - \- CPU: 32 MHz - APB: 32 MHz
- - None
  - Min values for both frequencies set with `esp_pm_configure`{.interpreted-text role="cpp:func"}
- - `2`{.interpreted-text role="rspan"} 64
  - `ESP_PM_CPU_FREQ_MAX` acquired
  - \- CPU: 64 MHz - APB: 32 MHz
- - `ESP_PM_APB_FREQ_MAX` acquired, `ESP_PM_CPU_FREQ_MAX` not acquired
  - \- CPU: 32 MHz - APB: 32 MHz
- - None
  - Min values for both frequencies set with `esp_pm_configure`{.interpreted-text role="cpp:func"}
- - `2`{.interpreted-text role="rspan"} 48
  - `ESP_PM_CPU_FREQ_MAX` acquired
  - \- CPU: 48 MHz - APB: 32 MHz
- - `ESP_PM_APB_FREQ_MAX` acquired, `ESP_PM_CPU_FREQ_MAX` not acquired
  - \- CPU: 32 MHz - APB: 32 MHz
- - None
  - Min values for both frequencies set with `esp_pm_configure`{.interpreted-text role="cpp:func"}
:::
