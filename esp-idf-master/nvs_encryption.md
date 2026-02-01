---
original_file_path: api-reference/storage/nvs_encryption.rst
---

# NVS Encryption

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

This guide provides an overview of the NVS encryption feature. NVS encryption helps to achieve secure storage on the device flash memory.

Data stored in NVS partitions can be encrypted using XTS-AES in the manner similar to the one mentioned in disk encryption standard IEEE P1619. For the purpose of encryption, each entry is treated as one `sector` and relative address of the entry (w.r.t., partition-start) is fed to the encryption algorithm as `sector-number`.

::: only
SOC_HMAC_SUPPORTED

NVS encryption can be facilitated by enabling `CONFIG_NVS_ENCRYPTION`{.interpreted-text role="ref"} and `CONFIG_NVS_SEC_KEY_PROTECTION_SCHEME`{.interpreted-text role="ref"} \> `CONFIG_NVS_SEC_KEY_PROTECT_USING_FLASH_ENC` or `CONFIG_NVS_SEC_KEY_PROTECT_USING_HMAC` depending on the scheme to be used.
:::

## NVS Encryption: Flash Encryption-Based Scheme {#nvs_encr_flash_enc_scheme}

In this scheme, the keys required for NVS encryption are stored in yet another partition, which is protected using `Flash Encryption <../../security/flash-encryption>`{.interpreted-text role="doc"}. Therefore, enabling `Flash Encryption <../../security/flash-encryption>`{.interpreted-text role="doc"} becomes a prerequisite for NVS encryption here.

::: only
SOC_HMAC_SUPPORTED

NVS encryption should be enabled when `../../security/flash-encryption`{.interpreted-text role="doc"} is enabled because the Wi-Fi driver stores credentials (like SSID and passphrase) in the default NVS partition. It is important to encrypt them if platform-level encryption is already enabled.
:::

::: only
not SOC_HMAC_SUPPORTED

NVS encryption is enabled by default when `../../security/flash-encryption`{.interpreted-text role="doc"} is enabled. This is done because Wi-Fi driver stores credentials (like SSID and passphrase) in the default NVS partition. It is important to encrypt them as default choice if platform-level encryption is already enabled.
:::

For using NVS encryption using this scheme, the partition table must contain the `nvs_encr_key_partition`{.interpreted-text role="ref"}. Two partition tables containing the `nvs_encr_key_partition`{.interpreted-text role="ref"} are provided for NVS encryption under the partition table option (`menuconfig` \> `Partition Table`). They can be selected with the project configuration menu (`idf.py menuconfig`). Please refer to the example `security/flash_encryption`{.interpreted-text role="example"} for how to configure and use the NVS encryption feature.

### NVS Key Partition {#nvs_encr_key_partition}

An application requiring NVS encryption support (using the Flash Encryption-based scheme) needs to be compiled with a key-partition of the type `data` and subtype `nvs_keys`. This partition should be marked as `encrypted` and its size should be the minimum partition size (4 KB). Refer to `../../api-guides/partition-tables`{.interpreted-text role="doc"} for more details. Two additional partition tables which contain the `nvs_encr_key_partition`{.interpreted-text role="ref"} are provided under the partition table option (`menuconfig` \> `Partition Table`). They can be directly used for NVS encryption. The structure of these partitions is depicted below:

``` none
+-----------+--------------+-------------+----+
|              XTS encryption key (32)        |
+---------------------------------------------+
|              XTS tweak key (32)             |
+---------------------------------------------+
|                  CRC32 (4)                  |
+---------------------------------------------+
```

The XTS encryption keys in the `nvs_encr_key_partition`{.interpreted-text role="ref"} can be generated in one of the following two ways.

**Generate the keys on {IDF_TARGET_NAME} chip itself**

> - When NVS encryption is enabled, the `nvs_flash_init`{.interpreted-text role="cpp:func"} API function can be used to initialize the encrypted default NVS partition. The API function internally generates the XTS encryption keys on the ESP chip. The API function finds the first `nvs_encr_key_partition`{.interpreted-text role="ref"}.
> - Then the API function automatically generates and stores the NVS keys in that partition by making use of the `nvs_flash_generate_keys`{.interpreted-text role="cpp:func"} API function provided by `nvs_flash/include/nvs_flash.h`{.interpreted-text role="component_file"}. New keys are generated and stored only when the respective key partition is empty. The same key partition can then be used to read the security configurations for initializing a custom encrypted NVS partition with help of `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"}.
> - The API functions `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} and `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"} do not generate the keys internally. When these API functions are used for initializing encrypted NVS partitions, the keys can be generated after startup using the `nvs_flash_generate_keys`{.interpreted-text role="cpp:func"} API function provided by `nvs_flash.h`. The API function then writes those keys onto the key-partition in encrypted form.
>
> :::: note
> ::: title
> Note
> :::
>
> Please note that `nvs_keys` partition must be completely erased before you start the application in this approach. Otherwise the application may generate the `ESP_ERR_NVS_CORRUPT_KEY_PART`{.interpreted-text role="c:macro"} error code assuming that `nvs_keys` partition is not empty and contains malformatted data. You can use the following command for this: :
>
> ``` none
> parttool.py --port PORT --partition-table-file=PARTITION_TABLE_FILE --partition-table-offset PARTITION_TABLE_OFFSET erase_partition --partition-type=data --partition-subtype=nvs_keys
>
> # If Flash Encryption or Secure Boot are enabled then add "--esptool-erase-args=force" to suppress the error:
> # "Active security features detected, erasing flash is disabled as a safety measure.  Use --force to override ..."
> parttool.py --port PORT --esptool-erase-args=force --partition-table-file=PARTITION_TABLE_FILE --partition-table-offset PARTITION_TABLE_OFFSET erase_partition --partition-type=data --partition-subtype=nvs_keys
> ```
> ::::

**Use a pre-generated NVS key partition**

> This option will be required by the user when keys in the `nvs_encr_key_partition`{.interpreted-text role="ref"} are not generated by the application. The `nvs_encr_key_partition`{.interpreted-text role="ref"} containing the XTS encryption keys can be generated with the help of `NVS Partition Generator Utility </api-reference/storage/nvs_partition_gen>`{.interpreted-text role="doc"}. Then the user can store the pre-generated key partition on the flash with help of the following two commands:
>
> 1\. Build and flash the partition table :
>
> ``` none
> idf.py partition-table partition-table-flash
> ```
>
> 2\. Store the keys in the `nvs_encr_key_partition`{.interpreted-text role="ref"} (on the flash) with the help of `parttool.py <partition_table/parttool.py>`{.interpreted-text role="component_file"} (see Partition Tool section in `partition-tables </api-guides/partition-tables>`{.interpreted-text role="doc"} for more details) :
>
> ``` none
> parttool.py --port PORT --partition-table-offset PARTITION_TABLE_OFFSET write_partition --partition-name="name of nvs_key partition" --input NVS_KEY_PARTITION_FILE
>
> # If Flash Encryption or Secure Boot are enabled then add "--esptool-erase-args=force" to suppress the error:
> # "Active security features detected, erasing flash is disabled as a safety measure.  Use --force to override ..."
> parttool.py --port PORT --esptool-erase-args=force --partition-table-offset PARTITION_TABLE_OFFSET write_partition --partition-name="name of nvs_key partition" --input NVS_KEY_PARTITION_FILE
> ```
>
> :::: note
> ::: title
> Note
> :::
>
> If the device is encrypted in flash encryption development mode and you want to renew the NVS key partition, you need to tell `parttool.py<partition_table/parttool.py>`{.interpreted-text role="component_file"} to encrypt the NVS key partition and you also need to give it a pointer to the unencrypted partition table in your build directory (build/partition_table) since the partition table on the device is encrypted, too. You can use the following command: :
>
> parttool.py \--esptool-write-args encrypt \--port PORT \--partition-table-file=PARTITION_TABLE_FILE \--partition-table-offset PARTITION_TABLE_OFFSET write_partition \--partition-name=\"name of nvs_key partition\" \--input NVS_KEY_PARTITION_FILE
>
> \# If Flash Encryption or Secure Boot are enabled then add \"\--esptool-erase-args=force\" to suppress the error: \# \"Active security features detected, erasing flash is disabled as a safety measure. Use \--force to override \...\" parttool.py \--esptool-erase-args=force \--esptool-write-args encrypt \--port PORT \--partition-table-file=PARTITION_TABLE_FILE \--partition-table-offset PARTITION_TABLE_OFFSET write_partition \--partition-name=\"name of nvs_key partition\" \--input NVS_KEY_PARTITION_FILE
> ::::

Since the key partition is marked as `encrypted` and `Flash Encryption <../../security/flash-encryption>`{.interpreted-text role="doc"} is enabled, the bootloader will encrypt this partition using flash encryption key on the first boot.

It is possible for an application to use different keys for different NVS partitions and thereby have multiple key-partitions. However, it is a responsibility of the application to provide the correct key-partition and keys for encryption or decryption.

::::::::::: only
SOC_HMAC_SUPPORTED

## NVS Encryption: HMAC Peripheral-Based Scheme {#nvs_encr_hmac_scheme}

In this scheme, the XTS keys required for NVS encryption are derived from an HMAC key programmed in eFuse with the purpose `esp_efuse_purpose_t::ESP_EFUSE_KEY_PURPOSE_HMAC_UP`{.interpreted-text role="cpp:enumerator"}. Since the encryption keys are derived at runtime, they are not stored anywhere in the flash. Thus, this feature does not require a separate `nvs_encr_key_partition`{.interpreted-text role="ref"}.

:::: note
::: title
Note
:::

This scheme enables us to achieve secure storage on {IDF_TARGET_NAME} **without enabling flash encryption**.
::::

:::: important
::: title
Important
:::

Please take note that this scheme uses one eFuse block for storing the HMAC key required for deriving the encryption keys.
::::

- When NVS encryption is enabled, the `nvs_flash_init`{.interpreted-text role="cpp:func"} API function can be used to initialize the encrypted default NVS partition. The API function first checks whether an HMAC key is present at `CONFIG_NVS_SEC_HMAC_EFUSE_KEY_ID`{.interpreted-text role="ref"}.

:::: note
::: title
Note
:::

The valid range for the config `CONFIG_NVS_SEC_HMAC_EFUSE_KEY_ID`{.interpreted-text role="ref"} is from `0` (`hmac_key_id_t::HMAC_KEY0`{.interpreted-text role="cpp:enumerator"}) to `5` (`hmac_key_id_t::HMAC_KEY5`{.interpreted-text role="cpp:enumerator"}). By default, the config is set to `-1`, which have to be configured before building the user application.
::::

- If no key is found, a key is generated internally and stored at the eFuse block specified at `CONFIG_NVS_SEC_HMAC_EFUSE_KEY_ID`{.interpreted-text role="ref"}.
- If a key is found with the purpose `esp_efuse_purpose_t::ESP_EFUSE_KEY_PURPOSE_HMAC_UP`{.interpreted-text role="cpp:enumerator"}, the same is used for the derivation of the XTS encryption keys.
- If the specified eFuse block is found to be occupied with a key with a purpose other than `esp_efuse_purpose_t::ESP_EFUSE_KEY_PURPOSE_HMAC_UP`{.interpreted-text role="cpp:enumerator"}, an error is thrown.
- The API `nvs_flash_init`{.interpreted-text role="cpp:func"} then automatically generates the NVS keys on demand by using the `nvs_flash_generate_keys_v2`{.interpreted-text role="cpp:func"} API function provided by the `nvs_flash/include/nvs_flash.h`{.interpreted-text role="component_file"}. The same keys can also be used to read the security configurations (see `nvs_flash_read_security_cfg_v2`{.interpreted-text role="cpp:func"}) for initializing a custom encrypted NVS partition with help of `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"}.
- The API functions `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} and `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"} do not generate the keys internally. When these API functions are used for initializing encrypted NVS partitions, the keys can be generated after startup using the `nvs_flash_generate_keys_v2`{.interpreted-text role="cpp:func"} API function or take and populate the NVS security configuration structure `nvs_sec_cfg_t`{.interpreted-text role="cpp:type"} with `nvs_flash_read_security_cfg_v2`{.interpreted-text role="cpp:func"} and feed them into the above APIs.

:::: note
::: title
Note
:::

Users can program their own HMAC key in eFuse block beforehand by using the following command: :

idf.py -p PORT efuse-burn-key \<BLOCK_KEYN\> \<hmac_key_file.bin\> HMAC_UP
::::
:::::::::::

## Encrypted Read/Write

The same NVS API functions `nvs_get_*` or `nvs_set_*` can be used for reading of, and writing to an encrypted NVS partition as well.

**Encrypt the default NVS partition**

- To enable encryption for the default NVS partition, no additional step is necessary. When `CONFIG_NVS_ENCRYPTION`{.interpreted-text role="ref"} is enabled, the `nvs_flash_init`{.interpreted-text role="cpp:func"} API function internally performs some additional steps to enable encryption for the default NVS partition depending on the scheme being used (set by `CONFIG_NVS_SEC_KEY_PROTECTION_SCHEME`{.interpreted-text role="ref"}).
- For the flash encryption-based scheme, the first `nvs_encr_key_partition`{.interpreted-text role="ref"} found is used to generate the encryption keys while for the HMAC one, keys are generated using the HMAC key burnt in eFuse at `CONFIG_NVS_SEC_HMAC_EFUSE_KEY_ID`{.interpreted-text role="ref"} (refer to the API documentation for more details).

Alternatively, `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} API function can also be used to enable encryption for the default NVS partition.

**Encrypt a custom NVS partition**

- To enable encryption for a custom NVS partition, `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"} API function is used instead of `nvs_flash_init_partition`{.interpreted-text role="cpp:func"}.

- When `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} and `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"} API functions are used, the applications are expected to follow the steps below in order to perform NVS read/write operations with encryption enabled:

  > 1.  Populate the NVS security configuration structure `nvs_sec_cfg_t`{.interpreted-text role="cpp:type"}
  >
  >     > - For the Flash Encryption-based scheme
  >     >
  >     >   > - Find key partition and NVS data partition using `esp_partition_find*` API functions.
  >     >   > - Populate the `nvs_sec_cfg_t`{.interpreted-text role="cpp:type"} struct using the `nvs_flash_read_security_cfg`{.interpreted-text role="cpp:func"} or `nvs_flash_generate_keys`{.interpreted-text role="cpp:func"} API functions.
  >     >
  >     > ::: only
  >     > SOC_HMAC_SUPPORTED
  >     >
  >     > - For the HMAC-based scheme
  >     >
  >     >   > - Set the scheme-specific config data with `nvs_sec_config_hmac_t`{.interpreted-text role="cpp:type"} and register the HMAC-based scheme with the API `nvs_sec_provider_register_hmac`{.interpreted-text role="cpp:func"} which will also populate the scheme-specific handle (see `nvs_sec_scheme_t`{.interpreted-text role="cpp:type"}).
  >     >   > - Populate the `nvs_sec_cfg_t`{.interpreted-text role="cpp:type"} struct using the `nvs_flash_read_security_cfg_v2`{.interpreted-text role="cpp:func"} or `nvs_flash_generate_keys_v2`{.interpreted-text role="cpp:func"} API functions.
  >     >
  >     > ``` c
  >     > nvs_sec_cfg_t cfg = {};
  >     > nvs_sec_scheme_t *sec_scheme_handle = NULL;
  >     >
  >     > nvs_sec_config_hmac_t sec_scheme_cfg = {};
  >     > hmac_key_id_t hmac_key = HMAC_KEY0;
  >     > sec_scheme_cfg.hmac_key_id = hmac_key;
  >     >
  >     > ret = nvs_sec_provider_register_hmac(&sec_scheme_cfg, &sec_scheme_handle);
  >     > if (ret != ESP_OK) {
  >     >     return ret;
  >     > }
  >     >
  >     > ret = nvs_flash_read_security_cfg_v2(sec_scheme_handle, &cfg);
  >     > if (ret != ESP_OK) {
  >     >     if (ret == ESP_ERR_NVS_SEC_HMAC_KEY_NOT_FOUND) {
  >     >         ret = nvs_flash_generate_keys_v2(&sec_scheme_handle, &cfg);
  >     >         if (ret != ESP_OK) {
  >     >             ESP_LOGE(TAG, "Failed to generate NVS encr-keys!");
  >     >             return ret;
  >     >         }
  >     >     }
  >     >     ESP_LOGE(TAG, "Failed to read NVS security cfg!");
  >     >     return ret;
  >     > }
  >     > ```
  >     > :::
  >
  > 2.  Initialise NVS flash partition using the `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} or `nvs_flash_secure_init_partition`{.interpreted-text role="cpp:func"} API functions.
  >
  > 3.  Open a namespace using the `nvs_open`{.interpreted-text role="cpp:func"} or `nvs_open_from_partition`{.interpreted-text role="cpp:func"} API functions.
  >
  > 4.  Perform NVS read/write operations using `nvs_get_*` or `nvs_set_*`.
  >
  > 5.  Deinitialise an NVS partition using `nvs_flash_deinit`{.interpreted-text role="cpp:func"}.

::::: only
SOC_HMAC_SUPPORTED

:::: note
::: title
Note
:::

While using the HMAC-based scheme, the above workflow can be used without enabling any of the config options for NVS encryption - `CONFIG_NVS_ENCRYPTION`{.interpreted-text role="ref"}, `CONFIG_NVS_SEC_KEY_PROTECTION_SCHEME`{.interpreted-text role="ref"} -\> `CONFIG_NVS_SEC_KEY_PROTECT_USING_HMAC` and `CONFIG_NVS_SEC_HMAC_EFUSE_KEY_ID`{.interpreted-text role="ref"} to encrypt the default as well as custom NVS partitions with `nvs_flash_secure_init`{.interpreted-text role="cpp:func"} API.
::::
:::::

## NVS Security Provider

The component `nvs_sec_provider`{.interpreted-text role="component"} stores all the implementation-specific code for the NVS encryption schemes and would also accommodate any future schemes. This component acts as an interface to the `nvs_flash`{.interpreted-text role="component"} component for the handling of encryption keys. `nvs_sec_provider`{.interpreted-text role="component"} has a configuration menu of its own, based on which the selected security scheme and the corresponding settings are registered for the `nvs_flash`{.interpreted-text role="component"} component.

::: only
SOC_HMAC_SUPPORTED

This component offers factory functions with which a particular security scheme can be registered without having to worry about the APIs to generate and read the encryption keys (e.g., `nvs_sec_provider_register_hmac`{.interpreted-text role="cpp:func"}). Refer to the `security/nvs_encryption_hmac`{.interpreted-text role="example"} example for API usage.
:::

:::: note
::: title
Note
:::

To use a custom implementation for NVS encryption key derivation or protection (instead of the ones provided by the `nvs_sec_provider`{.interpreted-text role="component"} component), select the `CONFIG_NVS_SEC_KEY_PROTECTION_SCHEME`{.interpreted-text role="ref"} -\> `CONFIG_NVS_SEC_KEY_PROTECT_NONE` configuration option.
::::

## API Reference

::: include-build-file
inc/nvs_sec_provider.inc
:::
