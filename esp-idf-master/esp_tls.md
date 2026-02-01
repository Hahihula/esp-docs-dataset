---
original_file_path: api-reference/protocols/esp_tls.rst
---

# ESP-TLS

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

The ESP-TLS component provides a simplified API interface for accessing the commonly used TLS functions. It supports common scenarios like CA certification validation, SNI, ALPN negotiation, and non-blocking connection among others. All the configurations can be specified in the `esp_tls_cfg_t` data structure. Once done, TLS communication can be conducted using the following APIs:

> - `esp_tls_init`{.interpreted-text role="cpp:func"}: for initializing the TLS connection handle.
> - `esp_tls_conn_new_sync`{.interpreted-text role="cpp:func"}: for opening a new blocking TLS connection.
> - `esp_tls_conn_new_async`{.interpreted-text role="cpp:func"}: for opening a new non-blocking TLS connection.
> - `esp_tls_conn_read`{.interpreted-text role="cpp:func"}: for reading from the connection.
> - `esp_tls_conn_write`{.interpreted-text role="cpp:func"}: for writing into the connection.
> - `esp_tls_conn_destroy`{.interpreted-text role="cpp:func"}: for freeing up the connection.

Any application layer protocol like HTTP1, HTTP2, etc can be executed on top of this layer.

## Application Example

Simple HTTPS example that uses ESP-TLS to establish a secure socket connection: `protocols/https_request`{.interpreted-text role="example"}.

## Tree Structure for ESP-TLS Component

``` none
├── esp_tls.c
├── esp_tls.h
├── esp_tls_mbedtls.c
├── esp_tls_wolfssl.c
└── private_include
    ├── esp_tls_mbedtls.h
    └── esp_tls_wolfssl.h
```

The ESP-TLS component has a file `esp-tls/esp_tls.h`{.interpreted-text role="component_file"} which contains the public API headers for the component. Internally, the ESP-TLS component operates using either MbedTLS or WolfSSL, which are SSL/TLS libraries. APIs specific to MbedTLS are present in `esp-tls/private_include/esp_tls_mbedtls.h`{.interpreted-text role="component_file"} and APIs specific to WolfSSL are present in `esp-tls/private_include/esp_tls_wolfssl.h`{.interpreted-text role="component_file"}.

## TLS Server Verification {#esp_tls_server_verification}

ESP-TLS provides multiple options for TLS server verification on the client side. The ESP-TLS client can verify the server by validating the peer\'s server certificate or with the help of pre-shared keys. The user should select only one of the following options in the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure for TLS server verification. If no option is selected, the client will return a fatal error by default during the TLS connection setup.

> - **cacert_buf** and **cacert_bytes**: The CA certificate can be provided in a buffer to the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure. The ESP-TLS uses the CA certificate present in the buffer to verify the server. The following variables in the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure must be set.
>
>   > - `cacert_buf` - pointer to the buffer which contains the CA certification.
>   > - `cacert_bytes` - the size of the CA certificate in bytes.
>
> - **use_global_ca_store**: The `global_ca_store` can be initialized and set at once. Then it can be used to verify the server for all the ESP-TLS connections which have set `use_global_ca_store = true` in their respective `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure. See the API Reference section below for information regarding different APIs used for initializing and setting up the `global_ca_store`.
>
> - **crt_bundle_attach**: The ESP x509 Certificate Bundle API provides an easy way to include a bundle of custom x509 root certificates for TLS server verification. More details can be found at `ESP x509 Certificate Bundle </api-reference/protocols/esp_crt_bundle>`{.interpreted-text role="doc"}.
>
> - **psk_hint_key**: To use pre-shared keys for server verification, `CONFIG_ESP_TLS_PSK_VERIFICATION`{.interpreted-text role="ref"} should be enabled in the ESP-TLS menuconfig. Then the pointer to the PSK hint and key should be provided to the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure. The ESP-TLS will use the PSK for server verification only when no other option regarding server verification is selected.
>
> - **skip server verification**: This is an insecure option provided in the ESP-TLS for testing purposes. The option can be set by enabling `CONFIG_ESP_TLS_INSECURE`{.interpreted-text role="ref"} and `CONFIG_ESP_TLS_SKIP_SERVER_CERT_VERIFY`{.interpreted-text role="ref"} in the ESP-TLS menuconfig. When this option is enabled the ESP-TLS will skip server verification by default when no other options for server verification are selected in the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure.
>
>   :::: warning
>   ::: title
>   Warning
>   :::
>
>   If this option is enabled, there is a risk of establishing a TLS connection with a server that has a fake identity, unless the server certificate is provided through the API or other mechanisms like `ca_store`.
>   ::::

## SNI (Server Name Indication)

SNI is an extension to the TLS protocol that allows the client to specify the hostname it is connecting to during the TLS handshake. This is required when connecting to servers that host multiple domains on the same IP address.

**How to ensure SNI works properly:**

- SNI is enabled by default in ESP-TLS when using HTTPS connections.
- To explicitly set the SNI hostname, use the `common_name` field in `esp_tls_cfg_t`{.interpreted-text role="cpp:type"}. This ensures that the correct hostname is sent to the server during the handshake.
- The value of `common_name` must match the server certificate\'s CN (Common Name).
- The `skip_common_name` field should be set to `false` to ensure the server certificate is properly validated against the hostname. This is required for SNI to function correctly.

Example:

``` c
esp_tls_cfg_t cfg = {
    .cacert_buf = ...,
    .cacert_bytes = ...,
    .common_name = "example.com", // SNI hostname
    .skip_common_name = false,    // Ensure certificate is validated
};
```

## ESP-TLS Server Cert Selection Hook

The ESP-TLS component provides an option to set the server certification selection hook when using the MbedTLS stack. This provides an ability to configure and use a certificate selection callback during server handshake. The callback helps to select a certificate to present to the client based on the TLS extensions supplied in the client hello message, such as ALPN and SNI. To enable this feature, please enable `CONFIG_ESP_TLS_SERVER_CERT_SELECT_HOOK`{.interpreted-text role="ref"} in the ESP-TLS menuconfig.

The certificate selection callback can be configured in the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure as follows:

``` c
int cert_selection_callback(mbedtls_ssl_context *ssl)
{
    /* Code that the callback should execute */
    return 0;
}

esp_tls_cfg_t cfg = {
    cert_select_cb = cert_section_callback,
};
```

## Underlying SSL/TLS Library Options {#esp_tls_wolfssl}

The ESP-TLS component offers the option to use MbedTLS or WolfSSL as its underlying SSL/TLS library. By default, only MbedTLS is available and used, WolfSSL SSL/TLS library is also available publicly at <https://github.com/espressif/esp-wolfssl>. The repository provides the WolfSSL component in binary format, and it also provides a few examples that are useful for understanding the API. Please refer to the repository `README.md` for information on licensing and other options. Please see the below section for instructions on how to use WolfSSL in your project.

:::: note
::: title
Note
:::

As the library options are internal to ESP-TLS, switching the libraries will not change ESP-TLS specific code for a project.
::::

## How to Use WolfSSL with ESP-IDF

There are two ways to use WolfSSL in your project:

- Add WolfSSL as a component directly to your project. For this, go to your project directory and run:

  ``` none
  mkdir components
  cd components
  git clone --recursive https://github.com/espressif/esp-wolfssl.git
  ```

- Add WolfSSL as an extra component in your project.

  > 1.  Download WolfSSL with:
  >
  >     ``` none
  >     git clone --recursive https://github.com/espressif/esp-wolfssl.git
  >     ```
  >
  > 2.  Include ESP-WolfSSL in ESP-IDF with setting `EXTRA_COMPONENT_DIRS` in `CMakeLists.txt` of your project as done in [wolfssl/examples](https://github.com/espressif/esp-wolfssl/tree/master/examples). For reference see `optional_project_variable`{.interpreted-text role="ref"} in `build-system </api-guides/build-system>`{.interpreted-text role="doc"}.

After the above steps, you will have the option to choose WolfSSL as the underlying SSL/TLS library in the configuration menu of your project as follow:

``` none
idf.py menuconfig > ESP-TLS > SSL/TLS Library > Mbedtls/Wolfssl
```

## Comparison Between MbedTLS and WolfSSL

The following table shows a typical comparison between WolfSSL and MbedTLS when the `protocols/https_request`{.interpreted-text role="example"} example (which includes server authentication) is running with both SSL/TLS libraries and with all respective configurations set to default. For MbedTLS, the IN_CONTENT length and OUT_CONTENT length are set to 16384 bytes and 4096 bytes respectively.

  ------------------------------------------------------------------------
  Property                     WolfSSL               MbedTLS
  ---------------------------- --------------------- ---------------------
  Total Heap Consumed          \~ 19 KB              \~ 37 KB

  Task Stack Used              \~ 2.2 KB             \~ 3.6 KB

  Bin size                     \~ 858 KB             \~ 736 KB
  ------------------------------------------------------------------------

:::: note
::: title
Note
:::

These values can vary based on configuration options and version of respective libraries.
::::

## ATECC608A (Secure Element) with ESP-TLS

ESP-TLS provides support for using ATECC608A cryptoauth chip with ESP32 series of SoCs. The use of ATECC608A is supported only when ESP-TLS is used with MbedTLS as its underlying SSL/TLS stack. ESP-TLS uses MbedTLS as its underlying TLS/SSL stack by default unless changed manually.

:::: note
::: title
Note
:::

ATECC608A chip interfaced to ESP32 series must be already configured. For details, please refer to [esp_cryptoauth_utility](https://github.com/espressif/esp-cryptoauthlib/blob/master/esp_cryptoauth_utility/README.md#esp_cryptoauth_utility).
::::

To enable the secure element support, and use it in your project for TLS connection, you have to follow the below steps:

1)  Add [esp-cryptoauthlib](https://github.com/espressif/esp-cryptoauthlib) in your project, for details please refer [how to use esp-cryptoauthlib with ESP-IDF](https://github.com/espressif/esp-cryptoauthlib#how-to-use-esp-cryptoauthlib-with-esp-idf).

2)  Enable the menuconfig option `CONFIG_ESP_TLS_USE_SECURE_ELEMENT`{.interpreted-text role="ref"}:

    ``` none
    menuconfig > Component config > ESP-TLS > Use Secure Element (ATECC608A) with ESP-TLS
    ```

3)  Select type of ATECC608A chip with following option:

    ``` none
    menuconfig > Component config > esp-cryptoauthlib > Choose Type of ATECC608A chip
    ```

    To know more about different types of ATECC608A chips and how to obtain the type of ATECC608A connected to your ESP module, please visit [ATECC608A chip type](https://github.com/espressif/esp-cryptoauthlib/blob/master/esp_cryptoauth_utility/README.md#find-type-of-atecc608a-chip-connected-to-esp32-wroom32-se).

4)  Enable the use of ATECC608A in ESP-TLS by providing the following config option in `esp_tls_cfg_t`{.interpreted-text role="cpp:type"}:

    ``` c
    esp_tls_cfg_t cfg = {
        /* other configurations options */
        .use_secure_element = true,
    };
    ```

::::: only
SOC_DIG_SIGN_SUPPORTED

## Digital Signature with ESP-TLS

ESP-TLS provides support for using the Digital Signature (DS) with {IDF_TARGET_NAME}. Use of the DS for TLS is supported only when ESP-TLS is used with MbedTLS (default stack) as its underlying SSL/TLS stack. For more details on Digital Signature, please refer to the `Digital Signature (DS) </api-reference/peripherals/ds>`{.interpreted-text role="doc"}. The technical details of Digital Signature such as how to calculate private key parameters can be found in **{IDF_TARGET_NAME} Technical Reference Manual** \> **Digital Signature (DS)** \[[PDF]({IDF_TARGET_TRM_EN_URL}#digsig)\]. The DS peripheral must be configured before it can be used to perform Digital Signature, see `configure-the-ds-peripheral`{.interpreted-text role="ref"}.

The DS peripheral must be initialized with the required encrypted private key parameters, which are obtained when the DS peripheral is configured. ESP-TLS internally initializes the DS peripheral when provided with the required DS context, i.e., DS parameters. Please see the below code snippet for passing the DS context to the ESP-TLS context. The DS context passed to the ESP-TLS context should not be freed till the TLS connection is deleted.

``` c
#include "esp_tls.h"
esp_ds_data_ctx_t *ds_ctx;
/* initialize ds_ctx with encrypted private key parameters, which can be read from the nvs or provided through the application code */
esp_tls_cfg_t cfg = {
    .clientcert_buf = /* the client certification */,
    .clientcert_bytes = /* length of the client certification */,
    /* other configurations options */
    .ds_data = (void *)ds_ctx,
};
```

:::: note
::: title
Note
:::

When using Digital Signature for the TLS connection, along with the other required params, only the client certification ([clientcert_buf]{.title-ref}) and the DS params ([ds_data]{.title-ref}) are required and the client key ([clientkey_buf]{.title-ref}) can be set to NULL.
::::

- A mutual-authentication example that utilizes the DS peripheral is shipped with the standalone [espressif/mqtt](https://components.espressif.com/components/espressif/mqtt) component and internally relies on ESP-TLS for the TLS connection. Follow the component documentation to fetch and build that example.
:::::

::::: only
SOC_ECDSA_SUPPORTED

## ECDSA Peripheral with ESP-TLS {#ecdsa-peri-with-esp-tls}

ESP-TLS provides support for using the ECDSA peripheral with {IDF_TARGET_NAME}. The use of ECDSA peripheral is supported only when ESP-TLS is used with MbedTLS as its underlying SSL/TLS stack. The ECDSA private key should be present in the eFuse for using the ECDSA peripheral. Please refer to `ECDSA Guide <../peripherals/ecdsa>`{.interpreted-text role="doc"} for programming the ECDSA key in the eFuse.

This will enable the use of ECDSA peripheral for private key operations. As the client private key is already present in the eFuse, it need not be supplied to the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure. Please see the below code snippet for enabling the use of ECDSA peripheral for a given ESP-TLS connection.

``` c
#include "esp_tls.h"
esp_tls_cfg_t cfg = {
    .use_ecdsa_peripheral = true,
    .ecdsa_key_efuse_blk = 4,     // Low eFuse block for ECDSA key
    .ecdsa_key_efuse_blk_high = 5,   // High eFuse block for ECDSA key (SECP384R1 only)
    .ecdsa_curve = ESP_TLS_ECDSA_CURVE_SECP384R1, // set this to ESP_TLS_ECDSA_CURVE_SECP256R1 for SECP256R1 curve
};
```

:::: note
::: title
Note
:::

When using ECDSA peripheral with TLS, only `MBEDTLS_TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256` ciphersuite is supported. If using TLS v1.3, `MBEDTLS_TLS1_3_AES_128_GCM_SHA256` ciphersuite is supported.
::::
:::::

## Client Session Tickets {#esp_tls_client_session_tickets}

ESP-TLS supports client-side session resumption, which can significantly reduce the time and resources spent on full TLS handshakes for subsequent connections to the same server. This feature is available when ESP-TLS uses MbedTLS as its underlying SSL/TLS stack.

The mechanism for session resumption differs slightly between TLS versions:

- **TLS 1.2**: Session resumption can be achieved using session IDs (managed internally by the TLS stack) or session tickets (as per [RFC 5077](https://tools.ietf.org/html/rfc5077)). ESP-TLS focuses on the session ticket mechanism for explicit application control.
- **TLS 1.3**: Session resumption is accomplished exclusively through session tickets, which are sent by the server via a \"NewSessionTicket\" message after the main handshake is complete. Unlike TLS 1.2, these tickets can be sent at any time during the session, not just immediately after the handshake.

To enable and use client session tickets:

1.  Enable the Kconfig option `CONFIG_ESP_TLS_CLIENT_SESSION_TICKETS`{.interpreted-text role="ref"}.

2.  After a successful TLS connection (and handshake completion), retrieve the session ticket using `esp_tls_get_client_session`{.interpreted-text role="cpp:func"}.

    > - **For TLS 1.3**: Since session tickets can arrive from the server at any point after the handshake, an application might need to call `esp_tls_get_client_session`{.interpreted-text role="cpp:func"} periodically or after specific application-level exchanges if it wants to ensure it has the most recent ticket. Each new ticket received and processed by the TLS stack supersedes the previous one for future resumption attempts.

3.  Store this session ticket securely.

4.  For subsequent connections to the same server, provide the stored session ticket in the `esp_tls_cfg_t::client_session`{.interpreted-text role="cpp:member"} field.

5.  Remember to free the client session context using `esp_tls_free_client_session`{.interpreted-text role="cpp:func"} when it\'s no longer needed or before obtaining a new one.

``` c
#include "esp_tls.h"

// Global or persistent storage for the client session
esp_tls_client_session_t *saved_session = NULL;

void connect_to_server(bool use_saved_session_arg) {
    esp_tls_cfg_t cfg = {0}; // Initialize other config parameters as needed
    // ... set other cfg members like cacert_buf, common_name etc. ...

    if (use_saved_session_arg && saved_session) {
        cfg.client_session = saved_session;
        // ESP_LOGI(TAG, "Attempting connection with saved session ticket.");
    } else {
        // ESP_LOGI(TAG, "Attempting connection without a saved session ticket (full handshake).");
    }

    esp_tls_t *tls = esp_tls_init();
    if (!tls) {
        // ESP_LOGE(TAG, "Failed to initialize ESP-TLS handle.");
        return;
    }

    if (esp_tls_conn_http_new_sync("https://your-server.com", &cfg, tls) == 1) {
        // ESP_LOGI(TAG, "Connection successful.");

        // Always try to get/update the session ticket to have the latest one.
        // This is beneficial whether the connection was a new handshake or a resumption,
        // especially for TLS 1.3 where new tickets can arrive post-handshake.
        if (saved_session) {
            esp_tls_free_client_session(saved_session); // Free previous session if any
            saved_session = NULL;
        }
        saved_session = esp_tls_get_client_session(tls);
        if (saved_session) {
            // ESP_LOGI(TAG, "Successfully retrieved/updated client session ticket.");
        } else {
            // ESP_LOGW(TAG, "Failed to get client session ticket even after a successful connection.");
        }

        // ... do TLS communication ...

    }
    esp_tls_conn_destroy(tls);
}
```

:::: note
::: title
Note
:::

- The session ticket obtained from a server is typically valid for a limited time. The server dictates this lifetime.
- When attempting a connection using a stored session ticket, if the ticket is found to be invalid by the server (e.g., it has expired or is otherwise rejected), ESP-TLS will automatically attempt to perform a full TLS handshake to establish the connection. The application does not need to implement separate logic to retry the connection without the ticket in this scenario. A connection failure will only be reported if both the session resumption and the subsequent internal attempt at a full handshake are unsuccessful.
- The `esp_tls_client_session_t`{.interpreted-text role="cpp:type"} context should be freed using `esp_tls_free_client_session`{.interpreted-text role="cpp:func"} when it is no longer needed, or before a new session is obtained and stored in the same pointer.
- For TLS 1.3, be mindful that the server can send multiple NewSessionTicket messages during a connection. Each successful call to `esp_tls_get_client_session`{.interpreted-text role="cpp:func"} will provide the context of the latest ticket processed by the underlying TLS stack. It is the application\'s responsibility to manage and update its stored session if it wishes to use the newest tickets for resumption.
::::

## TLS Ciphersuites

ESP-TLS provides the ability to set a ciphersuites list in client mode. The TLS ciphersuites list informs the server about the supported ciphersuites for the specific TLS connection regardless of the TLS stack configuration. If the server supports any ciphersuite from this list, then the TLS connection will succeed; otherwise, it will fail.

You can set `ciphersuites_list` in the `esp_tls_cfg_t`{.interpreted-text role="cpp:type"} structure during client connection as follows:

``` c
/* ciphersuites_list must end with 0 and must be available in the memory scope active during the entire TLS connection */
static const int ciphersuites_list[] = {MBEDTLS_TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384, MBEDTLS_TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384, 0};
esp_tls_cfg_t cfg = {
    .ciphersuites_list = ciphersuites_list,
};
```

ESP-TLS will not check the validity of `ciphersuites_list` that was set, you should call `esp_tls_get_ciphersuites_list`{.interpreted-text role="cpp:func"} to get ciphersuites list supported in the TLS stack and cross-check it against the supplied list.

:::: note
::: title
Note
:::

This feature is supported only in the MbedTLS stack.
::::

## TLS Protocol Version

ESP-TLS provides the ability to set the TLS protocol version for the respective TLS connection. Once the version is specified, it should be exclusively used to establish the TLS connection. This provides an ability to route different TLS connections to different protocol versions like TLS 1.2 and TLS 1.3 at runtime.

:::: note
::: title
Note
:::

At the moment, the feature is supported only when ESP-TLS is used with MbedTLS as its underlying SSL/TLS stack.
::::

To set TLS protocol version with ESP-TLS, set `esp_tls_cfg_t::tls_version`{.interpreted-text role="cpp:member"} to the required protocol version from `esp_tls_proto_ver_t`{.interpreted-text role="cpp:type"}. If the protocol version field is not set, then the default policy is to allow TLS connection based on the server requirement.

The ESP-TLS connection can be configured to use the specified protocol version as follows:

``` c
#include "esp_tls.h"
esp_tls_cfg_t cfg = {
    .tls_version = ESP_TLS_VER_TLS_1_2,
};
```

## API Reference

::: include-build-file
inc/esp_tls.inc
:::

::: include-build-file
inc/esp_tls_errors.inc
:::
