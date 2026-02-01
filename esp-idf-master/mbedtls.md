---
original_file_path: api-reference/protocols/mbedtls.rst
---

# Mbed TLS

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

[Mbed TLS](https://github.com/Mbed-TLS/mbedtls) is a C library that implements cryptographic primitives, X.509 certificate manipulation and the SSL/TLS and DTLS protocols. Its small code footprint makes it suitable for embedded systems.

:::: note
::: title
Note
:::

ESP-IDF uses a [fork](https://github.com/espressif/mbedtls) of Mbed TLS which includes a few patches (related to hardware routines of certain modules like `bignum (MPI)` and `ECC`) over vanilla Mbed TLS.
::::

Mbed TLS supports TLS 1.2, TLS 1.3 and DTLS 1.2 communication by providing the following:

- TCP/IP communication functions: listen, connect, accept, read/write.
- SSL/TLS communication functions: init, handshake, read/write.
- X.509 functions: CRT, CRL and key handling
- Random number generation
- Hashing
- Encryption/decryption

:::: note
::: title
Note
:::

Mbed TLS v3.x.x series supports only TLS 1.2 and TLS 1.3 protocols. Support for SSL 3.0, TLS 1.0/1.1 and DTLS 1.0 has been removed (deprecated). TLS 1.3 is fully supported starting Mbed TLS v3.6.0 release, before this release some features were still in experimental state. Please refer to `Mbed TLS ChangeLog <mbedtls/mbedtls/ChangeLog>`{.interpreted-text role="component_file"} for more details.
::::

## Mbed TLS Documentation

For Mbed TLS documentation please refer to the following (upstream) pointers:

- [API Reference](https://mbed-tls.readthedocs.io/projects/api/en/v3.6.5/)
- [Knowledge Base](https://mbed-tls.readthedocs.io/en/latest/kb/)

## Mbed TLS Support in ESP-IDF

Please find the information about the Mbed TLS versions presented in different branches of ESP-IDF [here](https://github.com/espressif/mbedtls/wiki#mbed-tls-support-in-esp-idf).

:::: note
::: title
Note
:::

Please refer the `migration_guide_mbedtls`{.interpreted-text role="ref"} to migrate from Mbed TLS version 2.x to version 3.0 or greater.
::::

### Configuration Presets

ESP-IDF provides a preset-based configuration system for Mbed TLS to simplify setup and provide optimized starting points for different use cases. This system works alongside the existing manual configuration system and provides baseline configurations that can be further customized through menuconfig or additional configuration files.

+--------------------+-----------------------------------+---------------------------------------+
| Preset             | Use Case                          | Key Features                          |
+====================+===================================+=======================================+
| **Default**        | General purpose applications      | - TLS 1.2 & 1.3 support               |
|                    |                                   | - Certificate bundle enabled          |
|                    |                                   | - Hardware acceleration               |
|                    |                                   | - Full cipher suite support           |
+--------------------+-----------------------------------+---------------------------------------+
| **Minimal**        | Resource-constrained applications | - TLS 1.2 client only                 |
|                    |                                   | - RSA & PSK key exchange              |
|                    |                                   | - AES-128 CBC/CTR modes               |
|                    |                                   | - Basic X.509 parsing                 |
+--------------------+-----------------------------------+---------------------------------------+
| **Bluetooth (BT)** | Bluetooth applications            | - Optimized for Bluetooth LE security |
|                    |                                   | - ECC P-256 curve support             |
|                    |                                   | - Minimal TLS overhead                |
|                    |                                   | - Bluetooth-specific algorithms       |
+--------------------+-----------------------------------+---------------------------------------+

### Using Configuration Presets

Presets serve as **starting points** for your mbedTLS configuration. You can use them as-is or customize them further using standard ESP-IDF configuration methods.

To use a preset configuration, add the following line to your project\'s `CMakeLists.txt` file **before** the `project()` call:

``` cmake
# Include the default preset (recommended for most applications)
list(APPEND sdkconfig_defaults $ENV{IDF_PATH}/components/mbedtls/config/mbedtls_preset_default.conf)

# Or for resource-constrained applications
list(APPEND sdkconfig_defaults $ENV{IDF_PATH}/components/mbedtls/config/mbedtls_preset_minimal.conf)

# Or for Bluetooth applications
list(APPEND sdkconfig_defaults $ENV{IDF_PATH}/components/mbedtls/config/mbedtls_preset_bt.conf)

# Standard ESP-IDF project setup
include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(my_project)
```

:::: note
::: title
Note
:::

The preset configurations are located in `components/mbedtls/config/` and can be customized or used as a starting point for your own configurations.
::::

### Customizing Preset Configurations

After applying a preset, you can further customize the configuration using any of these methods:

**Method 1: Using menuconfig (Recommended)**

``` bash
# After applying a preset in CMakeLists.txt
idf.py menuconfig
```

Navigate to `Component Config` \> `mbedTLS` to modify any settings. Your changes will override the preset defaults.

**Method 2: Additional Configuration Files**

You can combine a preset with your own custom configuration by creating an additional configuration file:

``` cmake
# Use the minimal preset as a base, then add custom settings
list(APPEND SDKCONFIG_DEFAULTS
    $ENV{IDF_PATH}/components/mbedtls/config/mbedtls_preset_minimal.conf
    ${CMAKE_CURRENT_SOURCE_DIR}/my_custom_mbedtls.conf
)
```

### Migration from Manual Configuration

The preset system complements manual configuration. If you have an existing manually configured mbedTLS setup:

**Option 1: Keep Your Existing Configuration**

Your current manual configuration will continue to work without any changes.

**Option 2: Migrate to Preset + Customization**

1.  **Choose a base preset** that\'s closest to your current configuration.
2.  **Apply the preset** in your `CMakeLists.txt`.
3.  **Use menuconfig** to adjust settings to match your requirements.
4.  **Test thoroughly** to ensure functionality is maintained.

### Configuration Categories

The new mbedTLS configuration system is organized into logical categories for easier navigation:

**Core Configuration**

:   Basic mbedTLS settings including memory allocation, threading, and debug options.

**TLS Protocol Configuration**

:   TLS/DTLS protocol versions, modes (client/server), and protocol-specific features.

**Symmetric Ciphers**

:   Block ciphers (AES, ARIA, etc.), cipher modes (CBC, GCM, etc.), and symmetric cryptography.

**Asymmetric Ciphers**

:   RSA, ECC, and other public key cryptography algorithms.

**Hash Functions**

:   Message digest algorithms (SHA-256, SHA-512, etc.) and HMAC.

**Hardware Acceleration**

:   ESP32-specific hardware acceleration for cryptographic operations.

**Certificate Support**

:   X.509 certificate parsing, validation, and certificate bundle management.

## Application Examples

Examples in ESP-IDF use `/api-reference/protocols/esp_tls`{.interpreted-text role="doc"} which provides a simplified API interface for accessing the commonly used TLS functionality.

Refer to the examples `protocols/https_server/simple`{.interpreted-text role="example"} (simple HTTPS server) and `protocols/https_request`{.interpreted-text role="example"} (make HTTPS requests) for more information.

If you plan to use the Mbed TLS API directly, refer to the example `protocols/https_mbedtls`{.interpreted-text role="example"}. This example demonstrates how to establish an HTTPS connection using Mbed TLS by setting up a secure socket with a certificate bundle for verification.

## Alternatives

`/api-reference/protocols/esp_tls`{.interpreted-text role="doc"} acts as an abstraction layer over the underlying SSL/TLS library and thus has an option to use Mbed TLS or wolfSSL as the underlying library. By default, only Mbed TLS is available and used in ESP-IDF whereas wolfSSL is available publicly at <https://github.com/espressif/esp-wolfSSL> with the upstream submodule pointer.

Please refer to `ESP-TLS: Underlying SSL/TLS Library Options <esp_tls_wolfssl>`{.interpreted-text role="ref"} documentation for more information on this and comparison of Mbed TLS and wolfSSL.

## Important Config Options

The Mbed TLS configuration system supports preset configurations. Following is a brief list of important config options accessible at `Component Config` \> `mbedTLS`. The full list of config options can be found `here <CONFIG_MBEDTLS_MEM_ALLOC_MODE>`{.interpreted-text role="ref"}.

**Core Configuration:**

::: list

SOC_SHA_SUPPORTED

:   - `CONFIG_MBEDTLS_HARDWARE_SHA`{.interpreted-text role="ref"}: Support for hardware SHA acceleration

SOC_AES_SUPPORTED

:   - `CONFIG_MBEDTLS_HARDWARE_AES`{.interpreted-text role="ref"}: Support for hardware AES acceleration

SOC_MPI_SUPPORTED

:   - `CONFIG_MBEDTLS_HARDWARE_MPI`{.interpreted-text role="ref"}: Support for hardware MPI (bignum) acceleration

SOC_ECC_SUPPORTED

:   - `CONFIG_MBEDTLS_HARDWARE_ECC`{.interpreted-text role="ref"}: Support for hardware ECC acceleration

- `CONFIG_MBEDTLS_MEM_ALLOC_MODE`{.interpreted-text role="ref"}: Memory allocation strategy (Internal/External/Custom)
- `CONFIG_MBEDTLS_ASYMMETRIC_CONTENT_LEN`{.interpreted-text role="ref"}: Asymmetric in/out fragment length for memory optimization
- `CONFIG_MBEDTLS_DYNAMIC_BUFFER`{.interpreted-text role="ref"}: Enable dynamic TX/RX buffer allocation
- `CONFIG_MBEDTLS_DEBUG`{.interpreted-text role="ref"}: Enable mbedTLS debugging (useful for debugging)
:::

**TLS Protocol Configuration:**

::: list
- `CONFIG_MBEDTLS_TLS_ENABLED`{.interpreted-text role="ref"}: Enable TLS protocol support
- `CONFIG_MBEDTLS_SSL_PROTO_TLS1_2`{.interpreted-text role="ref"}: Support for TLS 1.2 (recommended)
- `CONFIG_MBEDTLS_SSL_PROTO_TLS1_3`{.interpreted-text role="ref"}: Support for TLS 1.3 (latest standard)
- `CONFIG_MBEDTLS_SSL_PROTO_DTLS`{.interpreted-text role="ref"}: Support for DTLS (UDP-based TLS)
- `CONFIG_MBEDTLS_CLIENT_SSL_SESSION_TICKETS`{.interpreted-text role="ref"}: Support for TLS Session Resumption (client session tickets)
- `CONFIG_MBEDTLS_SERVER_SSL_SESSION_TICKETS`{.interpreted-text role="ref"}: Support for TLS Session Resumption Server session tickets
- `CONFIG_MBEDTLS_SSL_ALPN`{.interpreted-text role="ref"}: Support for Application Layer Protocol Negotiation
- `CONFIG_MBEDTLS_SSL_SERVER_NAME_INDICATION`{.interpreted-text role="ref"}: Support for Server Name Indication (SNI)
:::

**Certificate Support:**

::: list
- `CONFIG_MBEDTLS_CERTIFICATE_BUNDLE`{.interpreted-text role="ref"}: Support for trusted root certificate bundle (more about this: `/api-reference/protocols/esp_crt_bundle`{.interpreted-text role="doc"})
- `CONFIG_MBEDTLS_X509_USE_C`{.interpreted-text role="ref"}: Enable X.509 certificate support
- `CONFIG_MBEDTLS_PEM_PARSE_C`{.interpreted-text role="ref"}: Read & Parse PEM formatted certificates
- `CONFIG_MBEDTLS_PEM_WRITE_C`{.interpreted-text role="ref"}: Write PEM formatted certificates
- `CONFIG_MBEDTLS_X509_CRT_PARSE_C`{.interpreted-text role="ref"}: Parse X.509 certificates
- `CONFIG_MBEDTLS_X509_CRL_PARSE_C`{.interpreted-text role="ref"}: Parse X.509 certificate revocation lists
:::

**Cryptographic Algorithms:**

::: list
- `CONFIG_MBEDTLS_AES_C`{.interpreted-text role="ref"}: AES block cipher support
- `CONFIG_MBEDTLS_RSA_C`{.interpreted-text role="ref"}: RSA public key cryptosystem
- `CONFIG_MBEDTLS_ECP_C`{.interpreted-text role="ref"}: Elliptic Curve Cryptography support
- `CONFIG_MBEDTLS_ECDSA_C`{.interpreted-text role="ref"}: Elliptic Curve Digital Signature Algorithm
- `CONFIG_MBEDTLS_ECDH_C`{.interpreted-text role="ref"}: Elliptic Curve Diffie-Hellman key exchange
- `CONFIG_MBEDTLS_SHA256_C`{.interpreted-text role="ref"}: SHA-256 hash function
- `CONFIG_MBEDTLS_SHA512_C`{.interpreted-text role="ref"}: SHA-512 hash function
- `CONFIG_MBEDTLS_GCM_C`{.interpreted-text role="ref"}: Galois/Counter Mode for authenticated encryption
:::

:::: note
::: title
Note
:::

The new configuration structure provides better organization with categories like \"Core Configuration\", \"TLS Protocol Configuration\", \"Symmetric Ciphers\", \"Asymmetric Ciphers\", \"Hash Functions\", and \"Hardware Acceleration\" for easier navigation and configuration management.
::::

### Debugging mbedTLS

To enable debugging, add these configurations:

``` kconfig
CONFIG_MBEDTLS_DEBUG=y
CONFIG_MBEDTLS_DEBUG_LEVEL=3
CONFIG_LOG_DEFAULT_LEVEL_DEBUG=y
```

### Performance Optimization

For optimal performance, **enable hardware acceleration** when available:

``` kconfig
CONFIG_MBEDTLS_HARDWARE_AES=y
CONFIG_MBEDTLS_HARDWARE_SHA=y
CONFIG_MBEDTLS_HARDWARE_MPI=y
CONFIG_MBEDTLS_HARDWARE_ECC=y
```

## Performance and Memory Tweaks

### Reducing Heap Usage {#reducing_ram_usage_mbedtls}

The following table shows typical memory usage with different configs when the `protocols/https_request`{.interpreted-text role="example"} example (with Server Validation enabled) is run with Mbed TLS as the SSL/TLS library.

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Mbed TLS Test                      Related Configs                                                                                                                                                                                             Heap Usage (approx.)
  ---------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------
  Default                            NA                                                                                                                                                                                                          42196 B

  Enable SSL Dynamic Buffer Length   `CONFIG_MBEDTLS_SSL_VARIABLE_BUFFER_LENGTH`{.interpreted-text role="ref"}                                                                                                                                   42120 B

  Disable Keep Peer Certificate      `CONFIG_MBEDTLS_SSL_KEEP_PEER_CERTIFICATE`{.interpreted-text role="ref"}                                                                                                                                    38533 B

  Enable Dynamic TX/RX Buffer        `CONFIG_MBEDTLS_DYNAMIC_BUFFER`{.interpreted-text role="ref"} `CONFIG_MBEDTLS_DYNAMIC_FREE_CONFIG_DATA`{.interpreted-text role="ref"} `CONFIG_MBEDTLS_DYNAMIC_FREE_CA_CERT`{.interpreted-text role="ref"}   22013 B
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

:::: note
::: title
Note
:::

These values are subject to change with changes in configuration options and versions of Mbed TLS.
::::

### Reducing Binary Size

Under `Component Config` \> `mbedTLS`, several Mbed TLS features are enabled by default. These can be disabled if not needed to save code size. More information is available in the `Minimizing Binary Size <minimizing_binary_mbedtls>`{.interpreted-text role="ref"} documentation.
