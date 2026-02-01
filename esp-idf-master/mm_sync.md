---
original_file_path: api-reference/system/mm_sync.rst
---

# Memory Synchronization

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

::: {.toctree maxdepth="1"}
:::

## Introduction

::: only
SOC_PSRAM_DMA_CAPABLE

{IDF_TARGET_NAME} can access its connected PSRAM via these ways:

- CPU
- DMA
:::

::: only
SOC_CACHE_INTERNAL_MEM_VIA_L1CACHE

{IDF_TARGET_NAME} can access its internal memory via these ways:

- CPU
- DMA
:::

By default, CPU accesses the above mentioned memory via cache. Whereas DMA accesses the memory directly, without going through cache.

This leads to potential cache data coherence issue:

- When a DMA transaction changes the content of a piece of memory, and the content has been cached already. Under this condition:

  > - CPU may read stale data.
  > - The stale data in the cache may be written back to the memory. The new data updated by the previous DMA transaction will be overwritten.

- CPU changes the content of an address. The content is in the cache, but not in the memory yet (cache will write back the content to the memory according to its own strategy). Under this condition:

  > - The next DMA transactions to read this content from the memory will get stale data.

There are three common methods to address such cache data coherence issue:

::: list
1.  Hardware based cache Coherent Interconnect, {IDF_TARGET_NAME} does not have such ability.
2.  Use the DMA buffer from non-cacheable memory. Non-cacheable memory refers to the type of memory that is accessed by CPU without going through cache.
3.  Explicitly call a memory synchronization API to writeback the content in the cache back to the memory, or invalidate the content in the cache.
:::

## Memory Synchronization Driver

The suggested way to deal with such cache data coherence issue is by using the memory synchronization API `esp_cache_msync`{.interpreted-text role="cpp:func"} provided by ESP-IDF [esp_mm]{.title-ref} component.

### Driver Concept

Direction of the cache memory synchronization:

- `ESP_CACHE_MSYNC_FLAG_DIR_C2M`{.interpreted-text role="c:macro"}, for synchronization from cache to memory.
- `ESP_CACHE_MSYNC_FLAG_DIR_M2C`{.interpreted-text role="c:macro"}, for synchronization from memory to cache.

Type of the cache memory synchronization:

- `ESP_CACHE_MSYNC_FLAG_TYPE_DATA`{.interpreted-text role="c:macro"}, for synchronization to a data address region.
- `ESP_CACHE_MSYNC_FLAG_TYPE_INST`{.interpreted-text role="c:macro"}, for synchronization to an instruction address region.

### Driver Behaviour

Calling `esp_cache_msync`{.interpreted-text role="cpp:func"} will do a synchronization between cache and memory. The first parameter [addr]{.title-ref} and the second parameter [size]{.title-ref} together describe the memory region that is to be synchronized. About the third parameter \`flags\`:

::: list
- `ESP_CACHE_MSYNC_FLAG_DIR_C2M`{.interpreted-text role="c:macro"}. With this flag, content in the specified address region is written back to the memory. This direction is usually used **after** the content of an address is updated by the CPU, e.g., a memset to the address. Operation in this direction should happen **before** a DMA operation to the same address.
- `ESP_CACHE_MSYNC_FLAG_DIR_M2C`{.interpreted-text role="c:macro"}. With this flag, content in the specified address region is invalidated from the cache. This direction is usually used **after** the content of an address is updated by the DMA. Operation in this direction should happen **before** a CPU read operation to the same address.
:::

The above two flags help select the synchronization direction. Specially, if neither of these two flags are used, `esp_cache_msync`{.interpreted-text role="cpp:func"} will by default select the `ESP_CACHE_MSYNC_FLAG_DIR_C2M`{.interpreted-text role="c:macro"} direction. Users are not allowed to set both of the two flags at the same time.

::: list
- `ESP_CACHE_MSYNC_FLAG_TYPE_DATA`{.interpreted-text role="c:macro"}.
- `ESP_CACHE_MSYNC_FLAG_TYPE_INST`{.interpreted-text role="c:macro"}.
:::

The above two flags help select the type of the synchronization address. Specially, if neither of these two flags are used, `esp_cache_msync`{.interpreted-text role="cpp:func"} will by default select the `ESP_CACHE_MSYNC_FLAG_TYPE_DATA`{.interpreted-text role="c:macro"} type. Users are not allowed to set both of the two flags at the same time.

::: list
- `ESP_CACHE_MSYNC_FLAG_INVALIDATE`{.interpreted-text role="c:macro"}. This flag is used to trigger a cache invalidation to the specified address region, after the region is written back to the memory. This flag is mainly used for `ESP_CACHE_MSYNC_FLAG_DIR_C2M`{.interpreted-text role="c:macro"} direction. For `ESP_CACHE_MSYNC_FLAG_DIR_M2C`{.interpreted-text role="c:macro"} direction, behaviour is the same as if the `ESP_CACHE_MSYNC_FLAG_INVALIDATE`{.interpreted-text role="c:macro"} flag is not set.
- `ESP_CACHE_MSYNC_FLAG_UNALIGNED`{.interpreted-text role="c:macro"}. This flag force the `esp_cache_msync`{.interpreted-text role="cpp:func"} API to do synchronization without checking the address and size alignment. For more details, see section [Address Alignment Requirement]{.title-ref} following.
:::

## Address Alignment Requirement

There is address and size alignment requirement (in bytes) for using `esp_cache_msync`{.interpreted-text role="cpp:func"}. The alignment requirement comes from cache.

- An address region whose start address and size both meet the cache memory synchronization alignment requirement is defined as an **aligned address region**.
- An address region whose start address or size does not meet the cache memory synchronization alignment requirement is defined as an **unaligned address region**.

By default, if you specify an unaligned address region, `esp_cache_msync`{.interpreted-text role="cpp:func"} will return an `ESP_ERR_INVALID_ARG`{.interpreted-text role="c:macro"} error, together with the required alignment.

### Warning for Address Alignment Requirement

You can set the `ESP_CACHE_MSYNC_FLAG_UNALIGNED`{.interpreted-text role="c:macro"} flag to bypass such check. Note you should be very careful about using this flag. Cache memory synchronization to an unaligned address region may silently corrupt the memory.

For example, assume:

- alignment requirement is 0x40 bytes.
- a call to `esp_cache_msync`{.interpreted-text role="cpp:func"}, with [ESP_CACHE_MSYNC_FLAG_DIR_M2C \| ESP_CACHE_MSYNC_FLAG_UNALIGNED]{.title-ref} flags, the specified address region is 0x4000_0020 \~ 0x4000_0060 (see **data C** in below graph).

Above settings will trigger a cache invalidation to the address region 0x4000_0000 \~ 0x4000_0080, see **sync item0** and **sync item1** in the below graph.

If the content in 0x4000_0000 \~ 0x4000_0020 (**data A** in the below graph) or 0x4000_0060 \~ 0x4000_0080 (**data B** in the below graph) are not written back to the memory yet, then these **data A** and **data B** will be discarded.

![image](/../_static/diagrams/mmu/cache_align_issue.png){.align-center}

## API Reference

### API Reference - ESP Msync Driver

::: include-build-file
inc/esp_cache.inc
:::
