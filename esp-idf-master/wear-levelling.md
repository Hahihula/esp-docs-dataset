---
original_file_path: api-reference/storage/wear-levelling.rst
---

# See Also

- `./fatfs`{.interpreted-text role="doc"}
- `../../api-guides/partition-tables`{.interpreted-text role="doc"}

# Application Examples

- `storage/wear_levelling`{.interpreted-text role="example"} demonstrates how to use the wear levelling library and FatFS library to store files in a partition, as well as write and read data from these files using POSIX and C library APIs.

# High-level API Reference

## Header Files

- `fatfs/vfs/esp_vfs_fat.h`{.interpreted-text role="component_file"}

High-level wear levelling functions `esp_vfs_fat_spiflash_mount_rw_wl`{.interpreted-text role="cpp:func"}, `esp_vfs_fat_spiflash_unmount_rw_wl`{.interpreted-text role="cpp:func"} and struct `esp_vfs_fat_mount_config_t`{.interpreted-text role="cpp:class"} are described in `./fatfs`{.interpreted-text role="doc"}.

# Mid-level API Reference

::: include-build-file
inc/wear_levelling.inc
:::
