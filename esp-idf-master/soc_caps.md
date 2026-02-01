---
original_file_path: api-reference/system/soc_caps.rst
---

# SoC Capability Macros

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

Different models of ESP chips integrate various hardware modules. Even the same type of module may have subtle differences across different chips. ESP-IDF provides a small \"database\" to describe the differences between chips (please note, only differences are described, not commonalities). The contents of this \"database\" are defined as macros in the **soc/soc_caps.h** file, referred to as **SoC capability macros**. Users can utilize these macros in their code with conditional compilation directives (such as `#if`) to control which code is actually compiled.

:::: note
::: title
Note
:::

Please note that the contents of **soc/soc_caps.h** are currently unstable and may undergo significant changes in the future.
::::

## Using SoC Capability Macros

We recommend accessing SoC capability macros indirectly through the following macro functions:

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Macro Function                                Description                                                    Example
  --------------------------------------------- -------------------------------------------------------------- --------------------------------------------------------
  `SOC_IS`{.interpreted-text role="c:macro"}    Determines the chip model                                      `#if SOC_IS(ESP32)` checks if the chip is ESP32

  `SOC_HAS`{.interpreted-text role="c:macro"}   Checks if the chip has a specific hardware module or feature   `#if SOC_HAS(DAC)` checks if the chip has a DAC module
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------

## API Reference

::: include-build-file
inc/soc_caps.inc
:::

::: include-build-file
inc/soc_caps_eval.inc
:::
