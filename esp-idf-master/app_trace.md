---
original_file_path: api-reference/system/app_trace.rst
---

# Application Level Tracing

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

ESP-IDF provides a useful feature for application behavior analysis called **Application Level Tracing**. The feature can be enabled in menuconfig and allows transfer of arbitrary data between the host and {IDF_TARGET_NAME} via JTAG interface with minimal overhead on program execution.

Developers can use this library to send application specific state of execution to the host, and receive commands or other types of information in the opposite direction at runtime. The main use cases of this library are:

1.  Collecting application specific data, see `app_trace-application-specific-tracing`{.interpreted-text role="ref"}.
2.  Lightweight logging to the host, see `app_trace-logging-to-host`{.interpreted-text role="ref"}.
3.  System behaviour analysis, see `app_trace-system-behaviour-analysis-with-segger-systemview`{.interpreted-text role="ref"}.

## Application Examples

- `system/app_trace_to_plot`{.interpreted-text role="example"} demonstrates how to use the Application Level Tracing Library to send and plot dummy sensor data to a host via JTAG, providing a faster alternative to logging via UART.
- `system/app_trace_basic`{.interpreted-text role="example"} demonstrates how to use the Application Level Tracing Library to log messages to a host via JTAG, providing a faster alternative to UART logs.

## API Reference

::: include-build-file
inc/esp_app_trace.inc
:::
