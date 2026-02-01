---
original_file_path: migration-guides/release-6.x/6.0/protocols.rst
---

# Protocols

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## JSON

### Removed Built-in JSON Component

The built-in `json` component has been removed from ESP-IDF. Users should migrate to using the `espressif/cjson` component from the [IDF Component Manager](https://components.espressif.com/).

#### Migration Steps

1.  **Remove json from CMakeLists.txt**

    In your component\'s `CMakeLists.txt`, remove `json` from the `REQUIRES` or `PRIV_REQUIRES` list:

    ``` cmake
    # Before
    idf_component_register(SRCS "main.c"
                           PRIV_REQUIRES json esp_http_server)

    # After
    idf_component_register(SRCS "main.c"
                           PRIV_REQUIRES esp_http_server)
    ```

2.  **Add espressif/cjson to idf_component.yml**

    Add the `espressif/cjson` dependency to your component\'s `idf_component.yml` file. If this file doesn\'t exist, create it in your component directory (e.g., `main/idf_component.yml`):

    ``` yaml
    dependencies:
      espressif/cjson: "^1.7.19"
    ```

3.  **No Code Changes Required**

    The API remains the same. Your existing code using cJSON functions will continue to work without modifications:

    ``` c
    #include "cJSON.h"

    // Existing code works unchanged
    cJSON *root = cJSON_Parse(json_string);
    cJSON *item = cJSON_GetObjectItem(root, "key");
    cJSON_Delete(root);
    ```

For more information:

- [espressif/cjson component](https://components.espressif.com/components/espressif/cjson)
- [cJSON on GitHub](https://github.com/espressif/idf-extra-components/tree/master/cjson)

## ESP-TLS

**Removed Deprecated API**

The deprecated `esp_tls_conn_http_new`{.interpreted-text role="cpp:func"} function has been removed. Use either:

- `esp_tls_conn_http_new_sync`{.interpreted-text role="cpp:func"} for blocking connections
- `esp_tls_conn_http_new_async`{.interpreted-text role="cpp:func"} for non-blocking connections

The new API requires you to create the `esp_tls_t`{.interpreted-text role="cpp:type"} structure using `esp_tls_init`{.interpreted-text role="cpp:func"} and provides better control over the connection process.

## ESP-Modbus

The Espressif ESP-Modbus Library (esp-modbus) supports Modbus communication in the networks based on RS485, Wi-Fi, and Ethernet interfaces.

The component `esp-modbus v2 (v2.x.x)` is the current supported component version:

- [ESP-Modbus component on GitHub](https://github.com/espressif/esp-modbus/tree/main)

### Documentation

- [ESP-MODBUS stable documentation v2.x.x](https://docs.espressif.com/projects/esp-modbus/en/stable)
- [Documentation for legacy version v1.x.x](https://docs.espressif.com/projects/esp-modbus/en/v1)

### Application Examples

Since ESP-IDF version v6.0, the examples for component `esp-modbus v1` which is obsolete have been removed from ESP-IDF.

- [legacy esp-modbus v1.x.x examples (esp-idf v5.5)](https://github.com/espressif/esp-idf/tree/release/v5.5/examples/protocols/modbus)

The examples below demonstrate the ESP-Modbus library of serial and TCP ports for both slave and master implementations respectively.

- [mb_serial_slave](https://github.com/espressif/esp-modbus/tree/main/examples/serial/mb_serial_slave) - demonstrates how to use {IDF_TARGET_NAME} as a Modbus serial slave device with the esp-modbus stack, enabling an external Modbus host to read and write device parameters using the Modbus protocol.
- [mb_serial_master](https://github.com/espressif/esp-modbus/tree/main/examples/serial/mb_serial_master) - demonstrates how to use the esp-modbus stack port on {IDF_TARGET_NAME} as a Modbus serial master device, capable of reading and writing values from slave devices in a Modbus segment.
- [mb_tcp_slave](https://github.com/espressif/esp-modbus/tree/main/examples/tcp/mb_tcp_slave) - demonstrates the esp-modbus TCP slave stack port, allowing an external Modbus host to read and write device parameters via the Modbus protocol.
- [mb_tcp_master](https://github.com/espressif/esp-modbus/tree/main/examples/tcp/mb_tcp_master) - demonstrates how to use the esp-modbus stack port on {IDF_TARGET_NAME} as a Modbus TCP master device, capable of reading and writing values from slave devices in a Modbus network.

Please refer to the `README.md` documents of each specific example for details.

### Discussions

- [Discussions for version v2](https://github.com/espressif/esp-modbus/discussions)

## ESP-MQTT

Breaking change: ESP-MQTT moved to a managed component and example set updated.

- The ESP-MQTT component has been removed from ESP-IDF and is now a managed component: `espressif/mqtt`.
  - To add the component to an application, run `idf.py add-dependency espressif/mqtt`.
  - Include headers and APIs remain the same (`mqtt_client.h`), but the component is fetched via the Component Manager.
- Example changes in ESP-IDF:
  - Legacy MQTT TLS examples under `examples/protocols/mqtt/ssl*` were removed.
  - New reference examples are available:
    - `examples/protocols/mqtt`: MQTT over TLS.
    - `examples/protocols/mqtt5`: MQTT v5.0 over TLS.
