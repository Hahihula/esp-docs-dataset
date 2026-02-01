---
original_file_path: api-reference/storage/partition.rst
---

# Partitions API

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

The `esp_partition` component has higher-level API functions which work with partitions defined in the `/api-guides/partition-tables`{.interpreted-text role="doc"}. These APIs are based on lower level API provided by `/api-reference/peripherals/spi_flash/index`{.interpreted-text role="doc"}.

## Partition Table API {#flash-partition-apis}

ESP-IDF projects use a partition table to maintain information about various regions of SPI flash memory (bootloader, various application binaries, data, filesystems). More information can be found in `/api-guides/partition-tables`{.interpreted-text role="doc"}.

This component provides API functions to enumerate partitions found in the partition table and perform operations on them. These functions are declared in `esp_partition.h`:

- `esp_partition_find`{.interpreted-text role="cpp:func"} checks a partition table for entries with specific type, returns an opaque iterator.
- `esp_partition_get`{.interpreted-text role="cpp:func"} returns a structure describing the partition for a given iterator.
- `esp_partition_next`{.interpreted-text role="cpp:func"} shifts the iterator to the next found partition.
- `esp_partition_iterator_release`{.interpreted-text role="cpp:func"} releases iterator returned by `esp_partition_find`{.interpreted-text role="cpp:func"}.
- `esp_partition_find_first`{.interpreted-text role="cpp:func"} is a convenience function which returns the structure describing the first partition found by `esp_partition_find`{.interpreted-text role="cpp:func"}.
- `esp_partition_read`{.interpreted-text role="cpp:func"}, `esp_partition_write`{.interpreted-text role="cpp:func"}, `esp_partition_erase_range`{.interpreted-text role="cpp:func"} are equivalent to `esp_flash_read`{.interpreted-text role="cpp:func"}, `esp_flash_write`{.interpreted-text role="cpp:func"}, `esp_flash_erase_region`{.interpreted-text role="cpp:func"}, but operate within partition boundaries.

## Application Examples

- `storage/partition_api/partition_ops`{.interpreted-text role="example"} demonstrates how to perform read, write, and erase operations on a partition table.
- `storage/parttool`{.interpreted-text role="example"} demonstrates how to use the partitions tool to perform operations such as reading, writing, erasing partitions, retrieving partition information, and dumping the entire partition table.
- `storage/partition_api/partition_find`{.interpreted-text role="example"} demonstrates how to search the partition table and return matching partitions based on set constraints such as partition type, subtype, and label/name.
- `storage/partition_api/partition_mmap`{.interpreted-text role="example"} demonstrates how to configure the MMU, map a partition into memory address space for read operations, and verify the data written and read.

## See Also

- `../../api-guides/partition-tables`{.interpreted-text role="doc"}
- `../system/ota`{.interpreted-text role="doc"} provides high-level API for updating applications stored in flash.
- `nvs_flash`{.interpreted-text role="doc"} provides a structured API for storing small pieces of data in SPI flash.

## API Reference - Partition Table {#api-reference-partition-table}

::: include-build-file
inc/esp_partition.inc
:::
