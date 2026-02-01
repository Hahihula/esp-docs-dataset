---
original_file_path: api-guides/external-ram.rst
---

# Support for External RAM

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

::: {.toctree maxdepth="1"}
:::

## Introduction

{IDF_TARGET_PSRAM_VADDR_SIZE:default=\"Value not updated\", esp32=\"4 MB\", esp32s2=\"10.5 MB\", esp32s3=\"32 MB\", esp32p4=\"64 MB\"}

{IDF_TARGET_NAME} has a few hundred kilobytes of internal RAM, residing on the same die as the rest of the chip components. It can be insufficient for some purposes, so {IDF_TARGET_NAME} has the ability to use up to {IDF_TARGET_PSRAM_VADDR_SIZE} of virtual addresses for external PSRAM (pseudo-static RAM) memory. The external memory is incorporated in the memory map and, with certain restrictions, is usable in the same way as internal data RAM.

::: only
esp32s3

The {IDF_TARGET_PSRAM_VADDR_SIZE} virtual addresses are shared with flash instructions and rodata.
:::

## Hardware

{IDF_TARGET_NAME} supports PSRAM connected in parallel with the SPI flash chip. While {IDF_TARGET_NAME} is capable of supporting several types of RAM chips, ESP-IDF currently only supports Espressif branded PSRAM chips (e.g., ESP-PSRAM32, ESP-PSRAM64, etc).

::::::: note
::: title
Note
:::

::: only
esp32

Some PSRAM chips are 1.8 V devices and some are 3.3 V. The working voltage of the PSRAM chip must match the working voltage of the flash component. Consult the datasheet for your PSRAM chip and {IDF_TARGET_NAME} device to find out the working voltages. For a 1.8 V PSRAM chip, make sure to either set the MTDI pin to a high signal level on boot-up, or program {IDF_TARGET_NAME} eFuses to always use the VDD_SIO level of 1.8 V. Not doing this can damage the PSRAM and/or flash chip.
:::

::: only
esp32s2 or esp32s3

Some PSRAM chips are 1.8 V devices and some are 3.3 V. The working voltage of the PSRAM chip must match the working voltage of the flash component. Consult the datasheet for your PSRAM chip and {IDF_TARGET_NAME} device to find out the working voltages. For a 1.8 V PSRAM chip, make sure to either set the GPIO45 strapping pin to a high signal level on boot-up, or program {IDF_TARGET_NAME} eFuses to always use the VDD_SPI level of 1.8 V. Not doing this can damage the PSRAM and/or flash chip.
:::

::: only
esp32p4

Some PSRAM chips are 1.8 V devices and some are 3.3 V. Consult the datasheet for your PSRAM chip and {IDF_TARGET_NAME} device to find out the working voltages.

By default, the PSRAM is powered up by the on-chip LDO2. You can use `CONFIG_ESP_LDO_CHAN_PSRAM_DOMAIN`{.interpreted-text role="ref"} to switch the LDO channel accordingly. Set this value to -1 to use an external power supply, which means the on-chip LDO will not be used. By default, the PSRAM connected to LDO is set to the correct voltage based on the Espressif module used. You can still use `CONFIG_ESP_LDO_VOLTAGE_PSRAM_DOMAIN`{.interpreted-text role="ref"} to select the LDO output voltage if you are not using an Espressif module. When using an external power supply, this option does not exist.
:::
:::::::

:::: note
::: title
Note
:::

Espressif produces both modules and system-in-package chips that integrate compatible PSRAM and flash and are ready to mount on a product PCB. Consult the Espressif website for more information. If you are using a custom PSRAM chip, ESP-IDF SDK might not be compatible with it.
::::

For specific details about connecting the SoC or module pins to an external PSRAM chip, consult the SoC or module datasheet.

## Configuring External RAM {#external_ram_config}

:::: note
::: title
Note
:::

The `SPI RAM` configuration options are available only if the `esp_psram` component is included in the build. To include `SPI RAM` into your project, add the `esp_psram` component as a dependency in either `REQUIRES` or `PRIV_REQUIRES` when registering your component with `idf_component_register`.
::::

ESP-IDF fully supports the use of external RAM in applications. Once the external RAM is initialized at startup, ESP-IDF can be configured to integrate the external RAM in several ways:

::: list
- `external_ram_config_memory_map`{.interpreted-text role="ref"}
- `external_ram_config_capability_allocator`{.interpreted-text role="ref"}
- `external_ram_config_malloc`{.interpreted-text role="ref"} (default)
- `external_ram_config_bss`{.interpreted-text role="ref"}

\* `external_ram_config_noinit`{.interpreted-text role="ref"} :SOC_SPIRAM_XIP_SUPPORTED: \* `external_ram_config_xip`{.interpreted-text role="ref"}
:::

### Integrate RAM into the {IDF_TARGET_NAME} Memory Map {#external_ram_config_memory_map}

Select this option by choosing `Integrate RAM into memory map` from `CONFIG_SPIRAM_USE`{.interpreted-text role="ref"}.

This is the most basic option for external RAM integration. Most likely, you will need another, more advanced option.

During the ESP-IDF startup, external RAM is mapped into the data virtual address space. The address space is dynamically allocated. The length will be the minimum length between the PSRAM size and the available data virtual address space size.

Applications can manually place data in external memory by creating pointers to this region. So if an application uses external memory, it is responsible for all management of the external RAM: coordinating buffer usage, preventing corruption, etc.

It is recommended to access the PSRAM by ESP-IDF heap memory allocator (see next chapter).

### Add External RAM to the Capability Allocator {#external_ram_config_capability_allocator}

Select this option by choosing `Make RAM allocatable using heap_caps_malloc(..., MALLOC_CAP_SPIRAM)` from `CONFIG_SPIRAM_USE`{.interpreted-text role="ref"}.

When enabled, memory is mapped to data virtual address space and also added to the `capabilities-based heap memory allocator </api-reference/system/mem_alloc>`{.interpreted-text role="doc"} using `MALLOC_CAP_SPIRAM`.

To allocate memory from external RAM, a program should call `heap_caps_malloc(size, MALLOC_CAP_SPIRAM)`. After use, this memory can be freed by calling the normal `free()` function.

### Provide External RAM via malloc() {#external_ram_config_malloc}

Select this option by choosing `Make RAM allocatable using malloc() as well` from `CONFIG_SPIRAM_USE`{.interpreted-text role="ref"}. This is the default option.

In this case, memory is added to the capability allocator as described for the previous option. However, it is also added to the pool of RAM that can be returned by the standard `malloc()` function.

This allows any application to use the external RAM without having to rewrite the code to use `heap_caps_malloc(..., MALLOC_CAP_SPIRAM)`.

An additional configuration item, `CONFIG_SPIRAM_MALLOC_ALWAYSINTERNAL`{.interpreted-text role="ref"}, can be used to set the size threshold when a single allocation should prefer external memory:

- When allocating a size less than or equal to the threshold, the allocator will try internal memory first.
- When allocating a size larger than the threshold, the allocator will try external memory first.

If a suitable block of preferred internal/external memory is not available, the allocator will try the other type of memory.

Because some buffers can only be allocated in internal memory, a second configuration item `CONFIG_SPIRAM_MALLOC_RESERVE_INTERNAL`{.interpreted-text role="ref"} defines a pool of internal memory which is reserved for *only* explicitly internal allocations (such as memory for DMA use). Regular `malloc()` will not allocate from this pool. The `MALLOC_CAP_DMA <dma-capable-memory>`{.interpreted-text role="ref"} and `MALLOC_CAP_INTERNAL` flags can be used to allocate memory from this pool.

### Allow .bss Segment to Be Placed in External Memory {#external_ram_config_bss}

Enable this option by checking `CONFIG_SPIRAM_ALLOW_BSS_SEG_EXTERNAL_MEMORY`{.interpreted-text role="ref"}.

If enabled, the region of the data virtual address space where the PSRAM is mapped to will be used to store zero-initialized data (BSS segment) from the lwIP, net80211, libpp, wpa_supplicant and bluedroid ESP-IDF libraries.

Additional data can be moved from the internal BSS segment to external RAM by applying the macro `EXT_RAM_BSS_ATTR` to any static declaration (which is not initialized to a non-zero value).

It is also possible to place the BSS section of a component or a library to external RAM using linker fragment scheme `extram_bss`.

This option reduces the internal static memory used by the BSS segment.

Remaining external RAM can also be added to the capability heap allocator using the method shown above.

### Allow .noinit Segment to Be Placed in External Memory {#external_ram_config_noinit}

Enable this option by checking `CONFIG_SPIRAM_ALLOW_NOINIT_SEG_EXTERNAL_MEMORY`{.interpreted-text role="ref"}. If enabled, the region of the data virtual address space where the PSRAM is mapped to will be used to store non-initialized data. The values placed in this segment will not be initialized or modified even during startup or restart.

By applying the macro `EXT_RAM_NOINIT_ATTR`, data could be moved from the internal NOINIT segment to external RAM. Remaining external RAM can still be added to the capability heap allocator using the method shown above, `external_ram_config_capability_allocator`{.interpreted-text role="ref"}.

:::::: only
SOC_SPIRAM_XIP_SUPPORTED

::: only
esp32s2 or esp32s3

### Move Instructions in Flash to PSRAM

The `CONFIG_SPIRAM_FETCH_INSTRUCTIONS`{.interpreted-text role="ref"} option allows the flash `.text` sections (for instructions) to be placed in PSRAM.

By enabling the `CONFIG_SPIRAM_FETCH_INSTRUCTIONS`{.interpreted-text role="ref"} option,

- Instructions from the `.text` sections of flash are moved into PSRAM on system startup.
- The corresponding virtual memory range of those instructions will also be re-mapped to PSRAM.

### Move Read-Only Data in Flash to PSRAM

The `CONFIG_SPIRAM_RODATA`{.interpreted-text role="ref"} option allows the flash `.rodata` sections (for read only data) to be placed in PSRAM.

By enabling the `CONFIG_SPIRAM_RODATA`{.interpreted-text role="ref"} option,

- Instructions from the `.rodata` sections of flash are moved into PSRAM on system startup.
- The corresponding virtual memory range of those rodata will also be re-mapped to PSRAM.

### Execute In Place (XiP) from PSRAM {#external_ram_config_xip}

The `CONFIG_SPIRAM_XIP_FROM_PSRAM`{.interpreted-text role="ref"} is a helper option for you to select both the `CONFIG_SPIRAM_FETCH_INSTRUCTIONS`{.interpreted-text role="ref"} and `CONFIG_SPIRAM_RODATA`{.interpreted-text role="ref"}.

The benefits of XiP from PSRAM is:

- PSRAM access speed may be faster than flash access, so the overall application performance may be better. For example, if the PSRAM is an Octal mode (8-line PSRAM) and is configured to 80 MHz, then it is faster than a Quad flash (4-line flash) which is configured to 80 MHz.
- The cache will not be disabled during an SPI1 flash operation, thus optimizing the code execution performance during SPI1 flash operations. For ISRs, ISR callbacks and data which might be accessed during this period, you do not need to place them in internal RAM, thus internal RAM usage can be optimized. This feature is useful for high throughput peripheral involved applications to improve the performance during SPI1 flash operations.

`system/xip_from_psram`{.interpreted-text role="example"} demonstrates the usage of XiP from PSRAM, optimizing internal RAM usage and avoiding cache disabling during flash operations from user call (e.g., flash erase/read/write operations).
:::

:::: only
not (esp32s2 or esp32s3)

### Execute In Place (XiP) from PSRAM {#external_ram_config_xip}

The `CONFIG_SPIRAM_XIP_FROM_PSRAM`{.interpreted-text role="ref"} option enables the executable in place (XiP) from PSRAM feature. With this option sections that are normally placed in flash, `.text` (for instructions) and `.rodata` (for read only data), will be loaded in PSRAM.

With this option enabled, the cache will not be disabled during an SPI1 flash operation, so code that requires executing during an SPI1 flash operation does not have to be placed in internal RAM.

::: only
SOC_MMU_PER_EXT_MEM_TARGET

Since the flash and PSRAM in {IDF_TARGET_NAME} use two separate SPI buses, moving flash content to PSRAM will actually increase the load on the PSRAM MSPI bus. Therefore, the exact impact on performance will be dependent on your app usage of PSRAM.

The PSRAM bus can operate at a higher speed than the flash bus. For example, if the PSRAM is a HEX (16-line PSRAM on ESP32P4) running at 200 MHz, it is significantly faster than a Quad flash (4-line flash) running at 80 MHz.

If the instructions and data previously stored in flash are not accessed frequently, then enabling this option could improve performance. It is recommended to conduct performance profiling to evaluate how this option will affect your system.
:::
::::
::::::

## Restrictions

External RAM use has the following restrictions:

::: list
- When flash cache is disabled (for example, if the flash is being written to), the external RAM also becomes inaccessible. Any read operations from or write operations to it will lead to an illegal cache access exception. This is also the reason why ESP-IDF does not by default allocate any task stacks in external RAM (see below).

esp32s2

:   - External RAM cannot be used as a place to store DMA transaction descriptors or as a buffer for a DMA transfer to read from or write into. Therefore when External RAM is enabled, any buffer that will be used in combination with DMA must be allocated using `heap_caps_malloc(size, MALLOC_CAP_DMA | MALLOC_CAP_INTERNAL)` and can be freed using a standard `free()` call. Note that although {IDF_TARGET_NAME} has hardware support for DMA to or from external RAM, this is not yet supported in ESP-IDF.

esp32s3

:   - Although {IDF_TARGET_NAME} has hardware support for DMA to or from external RAM, there are still limitations:

esp32s3

:   - DMA transaction descriptors cannot be placed in PSRAM.

esp32s3

:   - The bandwidth that DMA accesses external RAM is very limited, especially when the core is trying to access the external RAM at the same time.

esp32s3

:   - You can configure `CONFIG_SPIRAM_SPEED`{.interpreted-text role="ref"} as 120 MHz for an octal PSRAM. The bandwidth will be improved. However there are still restrictions for this option. See `All Supported PSRAM Modes and Speeds <flash-psram-combination>`{.interpreted-text role="ref"} for more details.

- External RAM uses the same cache region as the external flash. This means that frequently accessed variables in external RAM can be read and modified almost as quickly as in internal RAM. However, when accessing large chunks of data (\> 32 KB), the cache can be insufficient, and speeds will fall back to the access speed of the external RAM. Moreover, accessing large chunks of data can \"push out\" cached flash, possibly making the execution of code slower afterwards.
- In general, external RAM will not be used as task stack memory. `xTaskCreate`{.interpreted-text role="cpp:func"} and similar functions will always allocate internal memory for stack and task TCBs.
:::

The option `CONFIG_FREERTOS_TASK_CREATE_ALLOW_EXT_MEM`{.interpreted-text role="ref"} can be used to allow placing task stacks into external memory. In these cases `xTaskCreateStatic`{.interpreted-text role="cpp:func"} must be used to specify a task stack buffer allocated from external memory, otherwise task stacks will still be allocated from internal memory.

## Failure to Initialize

By default, failure to initialize external RAM will cause the ESP-IDF startup to abort. This can be disabled by enabling the config item `CONFIG_SPIRAM_IGNORE_NOTFOUND`{.interpreted-text role="ref"}.

::: only
esp32 or esp32s2

If `CONFIG_SPIRAM_ALLOW_BSS_SEG_EXTERNAL_MEMORY`{.interpreted-text role="ref"} is enabled, the option to ignore failure is not available as the linker will have assigned symbols to external memory addresses at link time.
:::

::: only
not esp32

## Encryption

It is possible to enable automatic encryption for data stored in external RAM. When this is enabled any data read and written through the cache will automatically be encrypted or decrypted by the external memory encryption hardware.

This feature is enabled whenever flash encryption is enabled. For more information on how to enable and how it works see `Flash Encryption </security/flash-encryption>`{.interpreted-text role="doc"}.
:::

::: only
esp32

- Regarding stacks in PSRAM: For tasks that do not call ROM code in any way (directly or indirectly), the `CONFIG_FREERTOS_TASK_CREATE_ALLOW_EXT_MEM`{.interpreted-text role="ref"} option will eliminate the check in `xTaskCreateStatic`{.interpreted-text role="cpp:func"}, allowing a task\'s stack to be in external RAM. However, using this is **not advised**.
- When used at 80 MHz clock speed, external RAM must also occupy either the HSPI or VSPI bus. Select which SPI host will be used by `CONFIG_SPIRAM_OCCUPY_SPI_HOST`{.interpreted-text role="ref"}.

## Chip Revisions

There are some issues with certain revisions of ESP32 that have repercussions for use with external RAM. The issues are documented in the [ESP32 Series SoC Errata](https://www.espressif.com/sites/default/files/documentation/eco_and_workarounds_for_bugs_in_esp32_en.pdf) document. In particular, ESP-IDF handles the bugs mentioned in the following ways:

### ESP32 Rev v0.0

ESP-IDF has no workaround for the bugs in this revision of silicon, and it cannot be used to map external PSRAM into ESP32\'s main memory map.

### ESP32 Rev v1.0

The bugs in this revision of silicon cause issues if certain sequences of machine instructions operate on external memory. ([ESP32 Series SoC Errata](https://www.espressif.com/sites/default/files/documentation/eco_and_workarounds_for_bugs_in_esp32_en.pdf) \> CPU-3.2). As a workaround, the `-mfix-esp32-psram-cache-issue` flag has been added to the ESP32 GCC compiler such that these sequences are filtered out. As a result, the compiler only outputs code that can safely be executed. The `CONFIG_SPIRAM_CACHE_WORKAROUND`{.interpreted-text role="ref"} option can be used to enable this workaround.

Aside from linking to a recompiled version of Newlib with the additional flag, ESP-IDF also does the following:

- Avoids using some ROM functions
- Allocates static memory for the Wi-Fi stack

### ESP32 Rev v3.0

ESP32 rev v3.0 fixes the PSRAM cache issue found in rev v1.0. When `CONFIG_ESP32_REV_MIN`{.interpreted-text role="ref"} option is set to `rev v3.0`, compiler workarounds related to PSRAM will be disabled. For more information about ESP32 v3.0, see [ESP32 Chip Revision v3.0 User Guide](https://www.espressif.com/sites/default/files/documentation/ESP32_ECO_V3_User_Guide__EN.pdf).
:::
