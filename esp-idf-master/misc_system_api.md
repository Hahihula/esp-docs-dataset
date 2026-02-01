---
original_file_path: api-reference/system/misc_system_api.rst
---

# Miscellaneous System APIs

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

{IDF_TARGET_BASE_MAC_BLOCK: default=\"BLK1\", esp32=\"BLK0\"} {IDF_TARGET_CPU_RESET_DES: default=\"the CPU is reset\", esp32=\"both CPUs are reset\", esp32s3=\"both CPUs are reset\", esp32p4=\"both CPUs are reset\", esp32h4=\"both CPUs are reset\"}

## Software Reset

To perform software reset of the chip, the `esp_restart`{.interpreted-text role="cpp:func"} function is provided. When the function is called, execution of the program stops, {IDF_TARGET_CPU_RESET_DES}, the application is loaded by the bootloader and starts execution again.

Additionally, the `esp_register_shutdown_handler`{.interpreted-text role="cpp:func"} function can register a routine that will be automatically called before a restart (that is triggered by `esp_restart`{.interpreted-text role="cpp:func"}) occurs. This is similar to the functionality of `atexit` POSIX function.

## Reset Reason

ESP-IDF applications can be started or restarted due to a variety of reasons. To get the last reset reason, call `esp_reset_reason`{.interpreted-text role="cpp:func"} function. See description of `esp_reset_reason_t`{.interpreted-text role="cpp:type"} for the list of possible reset reasons.

## Heap Memory

Two heap-memory-related functions are provided:

- `esp_get_free_heap_size`{.interpreted-text role="cpp:func"} returns the current size of free heap memory.
- `esp_get_minimum_free_heap_size`{.interpreted-text role="cpp:func"} returns the minimum size of free heap memory that has ever been available (i.e., the smallest size of free heap memory in the application\'s lifetime).

Note that ESP-IDF supports multiple heaps with different capabilities. The functions mentioned in this section return the size of heap memory that can be allocated using the `malloc` family of functions. For further information about heap memory, see `Heap Memory Allocation <mem_alloc>`{.interpreted-text role="doc"}.

## MAC Address {#MAC-Address-Allocation}

These APIs allow querying and customizing MAC addresses for different supported network interfaces (e.g., Wi-Fi, Bluetooth, Ethernet).

To fetch the MAC address for a specific network interface (e.g., Wi-Fi, Bluetooth, Ethernet), call the function `esp_read_mac`{.interpreted-text role="cpp:func"}.

In ESP-IDF, the MAC addresses for the various network interfaces are calculated from a single **base MAC address**. By default, the Espressif base MAC address is used. This base MAC address is pre-programmed into the {IDF_TARGET_NAME} eFuse in the factory during production.

::::: only
not esp32s2

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Interface       MAC Address (4 universally administered, default)   MAC Address (2 universally administered)
  --------------- --------------------------------------------------- --------------------------------------------------------------------------------------------------
  Wi-Fi Station   base_mac                                            base_mac

  Wi-Fi SoftAP    base_mac, +1 to the last octet                      `Local MAC <local-mac-addresses>`{.interpreted-text role="ref"} (derived from Wi-Fi Station MAC)

  Bluetooth       base_mac, +2 to the last octet                      base_mac, +1 to the last octet

  Ethernet        base_mac, +3 to the last octet                      `Local MAC <local-mac-addresses>`{.interpreted-text role="ref"} (derived from Bluetooth MAC)
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------

:::: note
::: title
Note
:::

The `configuration <CONFIG_{IDF_TARGET_CFG_PREFIX}_UNIVERSAL_MAC_ADDRESSES>`{.interpreted-text role="ref"} configures the number of universally administered MAC addresses that are provided by Espressif.
::::
:::::

::::: only
esp32s2

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Interface       MAC Address (2 universally administered, default)                                                 MAC Address (1 universally administered)
  --------------- ------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------
  Wi-Fi Station   base_mac                                                                                          base_mac

  Wi-Fi SoftAP    base_mac, +1 to the last octet                                                                    `Local MAC <local-mac-addresses>`{.interpreted-text role="ref"} (derived from Wi-Fi Station MAC)

  Ethernet        `Local MAC <local-mac-addresses>`{.interpreted-text role="ref"} (derived from Wi-Fi SoftAP MAC)   `Local MAC <local-mac-addresses>`{.interpreted-text role="ref"} (derived from base_mac with +1 to last octet. Not recommended.)
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

:::: note
::: title
Note
:::

The `configuration <CONFIG_{IDF_TARGET_CFG_PREFIX}_UNIVERSAL_MAC_ADDRESSES>`{.interpreted-text role="ref"} configures the number of universally administered MAC addresses that are provided by Espressif.
::::
:::::

::::: only
not SOC_EMAC_SUPPORTED

:::: note
::: title
Note
:::

Although {IDF_TARGET_NAME} has no integrated Ethernet MAC, it is still possible to calculate an Ethernet MAC address. However, this MAC address can only be used with an external ethernet interface such as an SPI-Ethernet device. See `/api-reference/network/esp_eth`{.interpreted-text role="doc"}.
::::
:::::

### Custom Interface MAC

Sometimes you may need to define custom MAC addresses that are not generated from the base MAC address. To set a custom interface MAC address, use the `esp_iface_mac_addr_set`{.interpreted-text role="cpp:func"} function. This function allows you to overwrite the MAC addresses of interfaces set (or not yet set) by the base MAC address. Once a MAC address has been set for a particular interface, it will not be affected when the base MAC address is changed.

### Custom Base MAC

The default base MAC is pre-programmed by Espressif in eFuse {IDF_TARGET_BASE_MAC_BLOCK}. To set a custom base MAC instead, call the function `esp_iface_mac_addr_set`{.interpreted-text role="cpp:func"} with the `ESP_MAC_BASE` argument (or `esp_base_mac_addr_set`{.interpreted-text role="cpp:func"}) before initializing any network interfaces or calling the `esp_read_mac`{.interpreted-text role="cpp:func"} function. The custom MAC address can be stored in any supported storage device (e.g., flash, NVS).

The custom base MAC addresses should be allocated such that derived MAC addresses will not overlap. Based on the table above, users can configure the option `CONFIG_{IDF_TARGET_CFG_PREFIX}_UNIVERSAL_MAC_ADDRESSES`{.interpreted-text role="ref"} to set the number of valid universal MAC addresses that can be derived from the custom base MAC.

:::: note
::: title
Note
:::

It is also possible to call the function `esp_netif_set_mac`{.interpreted-text role="cpp:func"} to set the specific MAC used by a network interface after network initialization. But it is recommended to use the base MAC approach documented here to avoid the possibility of the original MAC address briefly appearing on the network before being changed.
::::

#### Custom MAC Address in eFuse

When reading custom MAC addresses from eFuse, ESP-IDF provides a helper function `esp_efuse_mac_get_custom`{.interpreted-text role="cpp:func"}. Users can also use `esp_read_mac`{.interpreted-text role="cpp:func"} with the `ESP_MAC_EFUSE_CUSTOM` argument. This loads the MAC address from eFuse BLK3. The `esp_efuse_mac_get_custom`{.interpreted-text role="cpp:func"} function assumes that the custom base MAC address is stored in the following format:

::::: only
esp32

  ------------------------------------------------------------------------------
  Field             \# of bits   Range of bits   Notes
  ----------------- ------------ --------------- -------------------------------
  Version           8            191:184         0: invalid, others --- valid

  Reserved          128          183:56          

  MAC address       48           55:8            

  MAC address CRC   8            7:0             CRC-8-CCITT, polynomial 0x07
  ------------------------------------------------------------------------------

:::: note
::: title
Note
:::

If the 3/4 coding scheme is enabled, all eFuse fields in this block must be burnt at the same time.
::::
:::::

::::: only
not esp32

  -----------------------------------------------------------------------
  Field                   \# of bits              Range of bits
  ----------------------- ----------------------- -----------------------
  MAC address             48                      200:248

  -----------------------------------------------------------------------

:::: note
::: title
Note
:::

The eFuse BLK3 uses RS-coding during burning, which means that all eFuse fields in this block must be burnt at the same time.
::::
:::::

Once custom eFuse MAC address has been obtained (using `esp_efuse_mac_get_custom`{.interpreted-text role="cpp:func"} or `esp_read_mac`{.interpreted-text role="cpp:func"}), you need to set it as the base MAC address. There are two ways to do it:

1.  Use an old API: call `esp_base_mac_addr_set`{.interpreted-text role="cpp:func"}.
2.  Use a new API: call `esp_iface_mac_addr_set`{.interpreted-text role="cpp:func"} with the `ESP_MAC_BASE` argument.

### Local Versus Universal MAC Addresses {#local-mac-addresses}

{IDF_TARGET_NAME} comes pre-programmed with enough valid Espressif universally administered MAC addresses for all internal interfaces. The table above shows how to calculate and derive the MAC address for a specific interface according to the base MAC address.

When using a custom MAC address scheme, it is possible that not all interfaces can be assigned with a universally administered MAC address. In these cases, a locally administered MAC address is assigned. Note that these addresses are intended for use on a single local network only.

See [this article](https://en.wikipedia.org/wiki/MAC_address#Universal_vs._local_(U/L_bit)) for the definition of locally and universally administered MAC addresses.

Function `esp_derive_local_mac`{.interpreted-text role="cpp:func"} is called internally to derive a local MAC address from a universal MAC address. The process is as follows:

1.  The U/L bit (bit value 0x2) is set in the first octet of the universal MAC address, creating a local MAC address.
2.  If this bit is already set in the supplied universal MAC address (i.e., the supplied \"universal\" MAC address was in fact already a local MAC address), then the first octet of the local MAC address is XORed with 0x4.

## Chip Version

`esp_chip_info`{.interpreted-text role="cpp:func"} function fills `esp_chip_info_t`{.interpreted-text role="cpp:class"} structure with information about the chip. This includes the chip revision, number of CPU cores, and a bit mask of features enabled in the chip.

## SDK Version {#idf-version-h}

`esp_get_idf_version`{.interpreted-text role="cpp:func"} returns a string describing the ESP-IDF version which is used to compile the application. This is the same value as the one available through `IDF_VER` variable of the build system. The version string generally has the format of `git describe` output.

To get the version at build time, additional version macros are provided. They can be used to enable or disable parts of the program depending on the ESP-IDF version.

- `ESP_IDF_VERSION_MAJOR`{.interpreted-text role="c:macro"}, `ESP_IDF_VERSION_MINOR`{.interpreted-text role="c:macro"}, `ESP_IDF_VERSION_PATCH`{.interpreted-text role="c:macro"} are defined to integers representing major, minor, and patch version.

- `ESP_IDF_VERSION_VAL`{.interpreted-text role="c:macro"} and `ESP_IDF_VERSION`{.interpreted-text role="c:macro"} can be used when implementing version checks:

  ``` c
  #include "esp_idf_version.h"

  #if ESP_IDF_VERSION >= ESP_IDF_VERSION_VAL(4, 0, 0)
      // enable functionality present in ESP-IDF v4.0
  #endif
  ```

## App Version

The application version is stored in `esp_app_desc_t`{.interpreted-text role="cpp:class"} structure. It is located in DROM sector and has a fixed offset from the beginning of the binary file. The structure is located after `esp_image_header_t`{.interpreted-text role="cpp:class"} and `esp_image_segment_header_t`{.interpreted-text role="cpp:class"} structures. The type of the field version is string and it has a maximum length of 32 chars.

To set the version in your project manually, you need to set the `PROJECT_VER` variable in the `CMakeLists.txt` of your project. In application `CMakeLists.txt`, put `set(PROJECT_VER "0.1.0.1")` before including `project.cmake`.

If the `CONFIG_APP_PROJECT_VER_FROM_CONFIG`{.interpreted-text role="ref"} option is set, the value of `CONFIG_APP_PROJECT_VER`{.interpreted-text role="ref"} will be used. Otherwise, if the `PROJECT_VER` variable is not set in the project, it will be retrieved either from the `$(PROJECT_PATH)/version.txt` file (if present) or using git command `git describe`. If neither is available, `PROJECT_VER` will be set to \"1\". Application can make use of this by calling `esp_app_get_description`{.interpreted-text role="cpp:func"} or `esp_ota_get_partition_description`{.interpreted-text role="cpp:func"} functions.

## Application Examples

- `system/base_mac_address`{.interpreted-text role="example"} demonstrates how to retrieve, set, and derive the base MAC address for each network interface on {IDF_TARGET_NAME} from non-volatile memory, using either the eFuse blocks or external storage.

## API Reference

::: include-build-file
inc/esp_system.inc
:::

::: include-build-file
inc/esp_idf_version.inc
:::

::: include-build-file
inc/esp_mac.inc
:::

::: include-build-file
inc/esp_chip_info.inc
:::

::: include-build-file
inc/esp_cpu.inc
:::

::: include-build-file
inc/esp_app_desc.inc
:::
