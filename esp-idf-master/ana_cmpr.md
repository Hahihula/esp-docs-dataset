---
original_file_path: api-reference/peripherals/ana_cmpr.rst
---

# Analog Comparator

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

{IDF_TARGET_ANA_CMPR_SRC_CHAN0: default=\"NOT UPDATED\", esp32h2=\"GPIO11\", esp32p4=\"GPIO52\", esp32c5=\"GPIO9\", esp32c61=\"GPIO9\"} {IDF_TARGET_ANA_CMPR_EXT_REF_CHAN0: default=\"NOT UPDATED\", esp32h2=\"GPIO10\", esp32p4=\"GPIO51\", esp32c5=\"GPIO8\", esp32c61=\"GPIO8\"} {IDF_TARGET_ANA_CMPR_SRC_CHAN1: default=\"NOT UPDATED\", esp32p4=\"GPIO54\"} {IDF_TARGET_ANA_CMPR_EXT_REF_CHAN1: default=\"NOT UPDATED\", esp32p4=\"GPIO53\"}

## Introduction

Analog comparator is a peripheral that can be used to compare a source signal with the internal reference voltage or an external reference signal.

Under the scenario of comparing the analog signals, the integrated analog comparator is a cost effective scheme to replace an operational amplifier. But unlike the continuous comparing of the operational amplifier, ESP analog comparator is driven by a source clock, which decides the sampling frequency.

Analog comparator on {IDF_TARGET_NAME} has {IDF_TARGET_SOC_ANA_CMPR_NUM} unit(s), the channels in the unit(s) are:

**UNIT0**

- Source Channel: {IDF_TARGET_ANA_CMPR_SRC_CHAN0}
- External Reference Channel: {IDF_TARGET_ANA_CMPR_EXT_REF_CHAN0}
- Internal Reference Channel: Range is 0% \~ 70% of the VDD, and the step is 10% of the VDD

::: only
esp32p4

**UNIT1**

- Source Channel: {IDF_TARGET_ANA_CMPR_SRC_CHAN1}
- External Reference Channel: {IDF_TARGET_ANA_CMPR_EXT_REF_CHAN1}
- Internal Reference Channel: Range 0% \~ 70% of the VDD, the step is 10% of the VDD
:::

## Functional Overview

The following sections of this document cover the typical steps to install and operate an analog comparator unit:

::: list
- `anacmpr-resource-allocation`{.interpreted-text role="ref"} - covers which parameters should be set up to get a unit handle and how to recycle the resources when it finishes working.
- `anacmpr-further-configurations`{.interpreted-text role="ref"} - covers the other configurations that might need to specify and what they are used for.
- `anacmpr-enable-and-disable-unit`{.interpreted-text role="ref"} - covers how to enable and disable the unit.
- `anacmpr-power-management`{.interpreted-text role="ref"} - describes how different source clock selections can affect power consumption.
- `anacmpr-iram-safe`{.interpreted-text role="ref"} - lists which functions are supposed to work even when the cache is disabled.
- `anacmpr-thread-safety`{.interpreted-text role="ref"} - lists which APIs are guaranteed to be thread safe by the driver.

\- `anacmpr-kconfig-options`{.interpreted-text role="ref"} - lists the supported Kconfig options that can be used to make a different effect on driver behavior. :SOC_ANA_CMPR_SUPPORT_ETM: - `anacmpr-etm-events`{.interpreted-text role="ref"} - covers how to create an analog comparator cross event.
:::

### Resource Allocation {#anacmpr-resource-allocation}

An analog comparator unit channel is represented by `ana_cmpr_handle_t`{.interpreted-text role="cpp:type"}. Each unit can support either an internal or an external reference.

To allocate the resource of the analog comparator unit, `ana_cmpr_new_unit`{.interpreted-text role="cpp:func"} need to be called to get the handle of the unit. Configurations `ana_cmpr_config_t`{.interpreted-text role="cpp:type"} need to be specified while allocating the unit:

- `ana_cmpr_config_t::unit`{.interpreted-text role="cpp:member"} selects the analog comparator unit.
- `ana_cmpr_config_t::clk_src`{.interpreted-text role="cpp:member"} selects the source clock for analog comparator, and it can affect the sampling frequency. Note that the clock source of the analog comparator comes from the IO MUX. It is shared with GPIO extension peripherals like SDM (Sigma-Delta Modulation) and Glitch Filter. The configuration will fail if you specify different clock sources for multiple GPIO extension peripherals. The default clock sources of these peripherals are same, and typically, we select `soc_periph_ana_cmpr_clk_src_t::ANA_CMPR_CLK_SRC_DEFAULT`{.interpreted-text role="cpp:enumerator"} as the clock source.
- `ana_cmpr_config_t::ref_src`{.interpreted-text role="cpp:member"} selects the reference source from internal voltage or external signal.
- `ana_cmpr_config_t::cross_type`{.interpreted-text role="cpp:member"} selects which kind of cross type can trigger the interrupt.

The function `ana_cmpr_new_unit`{.interpreted-text role="cpp:func"} can fail due to various errors such as insufficient memory, invalid arguments, etc. If a previously created analog comparator unit is no longer required, you should recycle it by calling `ana_cmpr_del_unit`{.interpreted-text role="cpp:func"}. It allows the underlying HW channel to be used for other purposes. Before deleting an analog comparator unit handle, you should disable it by `ana_cmpr_disable`{.interpreted-text role="cpp:func"} in advance, or make sure it has not enabled yet by `ana_cmpr_enable`{.interpreted-text role="cpp:func"}.

``` c
#include "driver/ana_cmpr.h"

ana_cmpr_handle_t cmpr = NULL;
ana_cmpr_config_t config = {
    .unit = 0,
    .clk_src = ANA_CMPR_CLK_SRC_DEFAULT,
    .ref_src = ANA_CMPR_REF_SRC_INTERNAL,
    .cross_type = ANA_CMPR_CROSS_ANY,
};
ESP_ERROR_CHECK(ana_cmpr_new_unit(&config, &cmpr));
// ...
ESP_ERROR_CHECK(ana_cmpr_del_unit(cmpr));
```

### Further Configurations {#anacmpr-further-configurations}

- `ana_cmpr_set_internal_reference`{.interpreted-text role="cpp:func"} - Specify the internal reference voltage when `ana_cmpr_ref_source_t::ANA_CMPR_REF_SRC_INTERNAL`{.interpreted-text role="cpp:enumerator"} is selected as reference source.

It requires `ana_cmpr_internal_ref_config_t::ref_volt`{.interpreted-text role="cpp:member"} to specify the voltage. The voltage is related to the VDD power supply, which can only support a certain fixed percentage of VDD. Currently on {IDF_TARGET_NAME}, the internal reference voltage can be range to 0 \~ 70% VDD with a step 10%.

``` c
#include "driver/ana_cmpr.h"

ana_cmpr_internal_ref_config_t ref_cfg = {
    .ref_volt = ANA_CMPR_REF_VOLT_50_PCT_VDD,
};
ESP_ERROR_CHECK(ana_cmpr_set_internal_reference(cmpr, &ref_cfg));
```

- `ana_cmpr_set_debounce`{.interpreted-text role="cpp:func"} - Set the debounce configuration.

It requires `ana_cmpr_debounce_config_t::wait_us`{.interpreted-text role="cpp:member"} to set the interrupt waiting time. The interrupt is disabled temporarily for `ana_cmpr_debounce_config_t::wait_us`{.interpreted-text role="cpp:member"} microseconds, so that the frequent triggering can be avoid while the source signal is crossing the reference signal. That is, the waiting time is supposed to be inverse ratio to the relative frequency between the source and reference. If the waiting time is set too short, it can not bypass the jitter totally, but if too long, the next crossing interrupt might be missed.

``` c
#include "driver/ana_cmpr.h"

ana_cmpr_debounce_config_t dbc_cfg = {
    .wait_us = 1,
};
ESP_ERROR_CHECK(ana_cmpr_set_debounce(cmpr, &dbc_cfg));
```

- `ana_cmpr_set_cross_type`{.interpreted-text role="cpp:func"} - Set the source signal cross type.

The initial cross type is set in `ana_cmpr_new_unit`{.interpreted-text role="cpp:func"}. This function can update the cross type, even in ISR context.

``` c
#include "driver/ana_cmpr.h"

ESP_ERROR_CHECK(ana_cmpr_set_cross_type(cmpr, ANA_CMPR_CROSS_POS));
```

- `ana_cmpr_register_event_callbacks`{.interpreted-text role="cpp:func"} - Register the callbacks.

Currently it supports `ana_cmpr_event_callbacks_t::on_cross`{.interpreted-text role="cpp:member"}, and it will be called when the crossing event (specified by `ana_cmpr_config_t::cross_type`{.interpreted-text role="cpp:member"}) occurs.

``` c
#include "driver/ana_cmpr.h"

static bool IRAM_ATTR example_ana_cmpr_on_cross_callback(ana_cmpr_handle_t cmpr,
                                                     const ana_cmpr_cross_event_data_t *edata,
                                                     void *user_ctx)
{
    // ...
    return false;
}
ana_cmpr_event_callbacks_t cbs = {
    .on_cross = example_ana_cmpr_on_cross_callback,
};
ESP_ERROR_CHECK(ana_cmpr_register_event_callbacks(cmpr, &cbs, NULL));
```

:::: note
::: title
Note
:::

When `CONFIG_ANA_CMPR_ISR_CACHE_SAFE`{.interpreted-text role="ref"} is enabled, you should guarantee that the callback context and involved data are in internal RAM by adding the attribute `IRAM_ATTR` (See more in `anacmpr-iram-safe`{.interpreted-text role="ref"}).
::::

### Enable and Disable Unit {#anacmpr-enable-and-disable-unit}

- `ana_cmpr_enable`{.interpreted-text role="cpp:func"} - Enable the analog comparator unit.
- `ana_cmpr_disable`{.interpreted-text role="cpp:func"} - Disable the analog comparator unit.

After the analog comparator unit is enabled and the crossing event interrupt is enabled, a power management lock will be acquired if the power management is enabled (see `anacmpr-power-management`{.interpreted-text role="ref"}). Under the **enable** state, only `ana_cmpr_set_internal_reference`{.interpreted-text role="cpp:func"} and `ana_cmpr_set_debounce`{.interpreted-text role="cpp:func"} can be called, other functions can only be called after the unit is disabled.

Calling `ana_cmpr_disable`{.interpreted-text role="cpp:func"} does the opposite.

### Power Management {#anacmpr-power-management}

When power management is enabled (i.e., `CONFIG_PM_ENABLE`{.interpreted-text role="ref"} is on), the system will adjust the APB frequency before going into Light-sleep mode, thus potentially changing the resolution of the analog comparator.

However, the driver can prevent the system from changing APB frequency by acquiring a power management lock of type `ESP_PM_NO_LIGHT_SLEEP`{.interpreted-text role="cpp:enumerator"}. Whenever the driver creates an analog comparator unit instance that has selected the clock source like `ANA_CMPR_CLK_SRC_DEFAULT`{.interpreted-text role="cpp:enumerator"} or `ANA_CMPR_CLK_SRC_XTAL`{.interpreted-text role="cpp:enumerator"}, the driver guarantees that the power management lock is acquired when enable the channel by `ana_cmpr_enable`{.interpreted-text role="cpp:func"}. Likewise, the driver releases the lock when `ana_cmpr_disable`{.interpreted-text role="cpp:func"} is called for that channel.

### IRAM Safe {#anacmpr-iram-safe}

By default, the analog comparator interrupt will be deferred when the cache is disabled for reasons like programming or erasing the flash. Thus the alarm interrupt will not get executed in time, which is not expected in a real-time application.

There is a Kconfig option `CONFIG_ANA_CMPR_ISR_CACHE_SAFE`{.interpreted-text role="ref"} that:

1.  Enables the interrupt being serviced even when cache is disabled.
2.  Places all functions that used by the ISR into IRAM.[^1]
3.  Places driver object into DRAM (in case it is allocated on PSRAM).

This allows the interrupt to run while the cache is disabled but comes at the cost of increased IRAM consumption.

There is a Kconfig option `CONFIG_ANA_CMPR_CTRL_FUNC_IN_IRAM`{.interpreted-text role="ref"} that can put commonly used IO control functions into IRAM as well. So that these functions can also be executable when the cache is disabled. These IO control functions are listed as follows:

- `ana_cmpr_set_internal_reference`{.interpreted-text role="cpp:func"}
- `ana_cmpr_set_debounce`{.interpreted-text role="cpp:func"}
- `ana_cmpr_set_cross_type`{.interpreted-text role="cpp:func"}

### Thread Safety {#anacmpr-thread-safety}

The factory function `ana_cmpr_new_unit`{.interpreted-text role="cpp:func"} is guaranteed to be thread safe by the driver, which means, it can be called from different RTOS tasks without protection by extra locks.

The following functions are allowed to run under ISR context. The driver uses a critical section to prevent them being called concurrently in both task and ISR:

- `ana_cmpr_set_internal_reference`{.interpreted-text role="cpp:func"}
- `ana_cmpr_set_debounce`{.interpreted-text role="cpp:func"}
- `ana_cmpr_set_cross_type`{.interpreted-text role="cpp:func"}

Other functions that take `ana_cmpr_handle_t`{.interpreted-text role="cpp:type"} as the first positional parameter, are not treated as thread safe. As a result, users should avoid calling them from multiple tasks.

### Kconfig Options {#anacmpr-kconfig-options}

- `CONFIG_ANA_CMPR_ISR_CACHE_SAFE`{.interpreted-text role="ref"} controls whether the default ISR handler can work when cache is disabled. See `anacmpr-iram-safe`{.interpreted-text role="ref"} for more information.
- `CONFIG_ANA_CMPR_CTRL_FUNC_IN_IRAM`{.interpreted-text role="ref"} controls where to place the analog comparator control functions (IRAM or flash). See `anacmpr-iram-safe`{.interpreted-text role="ref"} for more information.
- `CONFIG_ANA_CMPR_ENABLE_DEBUG_LOG`{.interpreted-text role="ref"} is used to enable the debug log output. Enabling this option increases the firmware binary size.

::: only
SOC_ANA_CMPR_SUPPORT_ETM

### ETM Events {#anacmpr-etm-events}

To create an analog comparator cross event, you need to include `driver/ana_cmpr_etm.h` additionally, and allocate the event by `ana_cmpr_new_etm_event`{.interpreted-text role="cpp:func"}. You can refer to `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} for how to connect an event to a task.
:::

## Application Example

- `peripherals/analog_comparator`{.interpreted-text role="example"} shows the basic usage of the analog comparator, and other potential usages like hysteresis comparator and SPWM generator.

## API Reference

::: include-build-file
inc/ana_cmpr.inc
:::

::: include-build-file
inc/ana_cmpr_types.inc
:::

[^1]: `ana_cmpr_event_callbacks_t::on_cross`{.interpreted-text role="cpp:member"} callback and the functions invoked by it should also be placed in IRAM. Please take care of them.
