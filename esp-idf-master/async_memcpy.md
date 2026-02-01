---
original_file_path: api-reference/system/async_memcpy.rst
---

# Asynchronous Memory Copy

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

{IDF_TARGET_NAME} has a DMA engine which can help to offload internal memory copy operations from the CPU in an asynchronous way.

The async memcpy API wraps all DMA configurations and operations. The signature of `esp_async_memcpy`{.interpreted-text role="cpp:func"} is almost the same as the standard libc `memcpy` function.

The DMA allows multiple memory copy requests to be queued up before the first one is completed, which allows overlap of computation and memory copy. Moreover, it is still possible to know the exact time when a memory copy request is completed by registering an event callback.

## Configure and Install Driver

There are several ways to install the async memcpy driver, depending on the underlying DMA engine:

::: list

SOC_CP_DMA_SUPPORTED

:   - `esp_async_memcpy_install_cpdma`{.interpreted-text role="cpp:func"} is used to install the async memcpy driver based on the CP DMA engine.

SOC_AHB_GDMA_SUPPORTED

:   - `esp_async_memcpy_install_gdma_ahb`{.interpreted-text role="cpp:func"} is used to install the async memcpy driver based on the AHB GDMA engine.

SOC_AXI_GDMA_SUPPORTED

:   - `esp_async_memcpy_install_gdma_axi`{.interpreted-text role="cpp:func"} is used to install the async memcpy driver based on the AXI GDMA engine.

- `esp_async_memcpy_install`{.interpreted-text role="cpp:func"} is a generic API to install the async memcpy driver with a default DMA engine. If the SoC has the CP DMA engine, the default DMA engine is CP DMA. Otherwise, the default DMA engine is AHB GDMA.
:::

Driver configuration is described in `async_memcpy_config_t`{.interpreted-text role="cpp:type"}:

- `backlog`{.interpreted-text role="cpp:member"}: This is used to configure the maximum number of memory copy transactions that can be queued up before the first one is completed. If this field is set to zero, then the default value 4 will be applied.
- `dma_burst_size`{.interpreted-text role="cpp:member"}: Set the burst size in a DMA burst transfer.
- `flags`{.interpreted-text role="cpp:member"}: This is used to enable some special driver features.

``` c
async_memcpy_config_t config = ASYNC_MEMCPY_DEFAULT_CONFIG();
// update the maximum data stream supported by underlying DMA engine
config.backlog = 8;
async_memcpy_handle_t driver = NULL;
ESP_ERROR_CHECK(esp_async_memcpy_install(&config, &driver)); // install driver with default DMA engine
```

## Send Memory Copy Request

`esp_async_memcpy`{.interpreted-text role="cpp:func"} is the API to send memory copy request to DMA engine. It must be called after driver is installed successfully. This API is thread safe, so it can be called from different tasks.

Different from the libc version of `memcpy`, you can optionally pass a callback to `esp_async_memcpy`{.interpreted-text role="cpp:func"}, so that you can be notified when the memory copy is finished. Note that the callback is executed in the ISR context, please make sure you will not call any blocking functions in the callback.

The prototype of the callback function is `async_memcpy_isr_cb_t`{.interpreted-text role="cpp:type"}. The callback function should only return true if it wakes up a high priority task by RTOS APIs like `xSemaphoreGiveFromISR`{.interpreted-text role="cpp:func"}.

``` c
// Callback implementation, running in ISR context
static bool my_async_memcpy_cb(async_memcpy_handle_t mcp_hdl, async_memcpy_event_t *event, void *cb_args)
{
    SemaphoreHandle_t sem = (SemaphoreHandle_t)cb_args;
    BaseType_t high_task_wakeup = pdFALSE;
    xSemaphoreGiveFromISR(semphr, &high_task_wakeup); // high_task_wakeup set to pdTRUE if some high priority task unblocked
    return high_task_wakeup == pdTRUE;
}

// Create a semaphore used to report the completion of async memcpy
SemaphoreHandle_t semphr = xSemaphoreCreateBinary();

// Called from user's context
ESP_ERROR_CHECK(esp_async_memcpy(driver_handle, to, from, copy_len, my_async_memcpy_cb, my_semaphore));
// Do something else here
xSemaphoreTake(my_semaphore, portMAX_DELAY); // Wait until the buffer copy is done
```

## Uninstall Driver

`esp_async_memcpy_uninstall`{.interpreted-text role="cpp:func"} is used to uninstall asynchronous memcpy driver. It is not necessary to uninstall the driver after each memcpy operation. If you know your application will not use this driver anymore, then this API can recycle the memory and other hardware resources for you.

::: only
SOC_ETM_SUPPORTED and SOC_GDMA_SUPPORT_ETM

## ETM Event

Async memory copy is able to generate an event when one async memcpy operation is done. This event can be used to interact with the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} module. You can call `esp_async_memcpy_new_etm_event`{.interpreted-text role="cpp:func"} to get the ETM event handle.

For how to connect the event to an ETM channel, please refer to the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} documentation.
:::

## API Reference

::: include-build-file
inc/esp_async_memcpy.inc
:::
