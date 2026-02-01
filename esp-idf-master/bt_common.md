---
original_file_path: migration-guides/release-5.x/5.4/bt_common.rst
---

# Bluetooth Common

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

The following Bluetooth Common header declarations have been moved:

::: only
esp32

- `/bt/include/esp32/include/esp_bt.h`{.interpreted-text role="component_file"}

  > - Move the declarations of `esp_wifi_bt_power_domain_on` and `esp_wifi_bt_power_domain_off` from `esp_bt.h` to `esp_phy_init.h`, since they belong to component `esp_phy` and are not expected to be used by customer.
:::

::: only
esp32c3 or esp32s3

- `/bt/include/esp32c3/include/esp_bt.h`{.interpreted-text role="component_file"}

  > - Move the declarations of `esp_wifi_bt_power_domain_on` and `esp_wifi_bt_power_domain_off` from `esp_bt.h` to `esp_phy_init.h`, since they belong to component `esp_phy` and are not expected to be used by customer.
:::
