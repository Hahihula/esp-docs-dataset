---
original_file_path: api-guides/code-quality/static-analyzer.rst
---

# Static Analyzer

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

A static analyzer is a tool that checks source code for errors and vulnerabilities without running it. It helps developers find issues early, improving code quality.

## GNU Static Analyzer

The GNU Static Analyzer is distributed with GCC (refer to [GCC documentation](https://gcc.gnu.org/onlinedocs/gcc/Static-Analyzer-Options.html)). It can be enabled with `CONFIG_COMPILER_STATIC_ANALYZER`{.interpreted-text role="ref"} to perform code checks during application builds.

### Suppressing Warnings

GNU Static Analyzer is still under development and may give some false-positive warnings. Here is an example of how to suppress unwanted warnings using IDF:

``` c
#include "esp_compiler.h"
/* .... */
  ESP_COMPILER_DIAGNOSTIC_PUSH_IGNORE("-Wanalyzer-null-dereference")
  *((volatile int *) 0) = 0;
  ESP_COMPILER_DIAGNOSTIC_POP("-Wanalyzer-null-dereference")
/* .... */
```

## Clang Static Analyzer

See `IDF Clang-Tidy <../../api-guides/tools/idf-clang-tidy>`{.interpreted-text role="doc"}
