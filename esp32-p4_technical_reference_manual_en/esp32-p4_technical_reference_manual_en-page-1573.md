

```markdown
## 34.7.2.5 GAIN Phase

Users check `KEYMNG_STATE` to confirm that the Key Manager is in the GAIN phase. In the GAIN phase, users extract the required key information based on the selected mode of the Key Manager.

### 1. Extract Key Information:

*   **Random Deploy Mode:**
    *   (a) Read `key_info` (512 bits) from `KEYMNG_PUBLIC_INFO_MEM`.

*   **AES Deploy Mode:**
    *   (a) Read `key_info` (512 bits) from `KEYMNG_PUBLIC_INFO_MEM`.

*   **ECDHO Deploy Mode:**
    *   (a) Read `key_info` (512 bits) from `KEYMNG_PUBLIC_INFO_MEM`.
    *   (b) Read `k2 * G` (512 bits) from `KEYMNG_ASSIST_INFO_MEM`.

*   **ECDH1 Deploy Mode:**
    *   (a) Read `key_info` (512 bits) from `KEYMNG_PUBLIC_INFO_MEM`.

*   **Private Key Recovery Mode:** no need to read any information.

*   **key_info Export Mode:**
    *   (a) Read `key_info` (512 bits) from `KEYMNG_PUBLIC_INFO_MEM`.

### 2. Transition to POST Phase:

Configure `KEYMNG_CONTINUE` to complete the GAIN phase and enter the POST phase.

## 34.7.2.6 POST Phase

Users need to wait for the POST phase to complete. This can be done using one of the following methods.

*   **Monitor `KEYMNG_STATE`:** Continuously check `KEYMNG_STATE` until it is no longer BUSY.
*   **Use Interrupt:** Enable the interrupt `KEYMNG_POST_DONE_INT` and handle the completion in the interrupt service routine.

## 34.8 Programming Examples

Based on the previous sections, we can outline a comprehensive chip deployment process. This section explains the operation procedures for the HUK Generator and Key Manager during two typical chip startup scenarios.

**Note:**
In this section, all configuration processes are described in a simplified manner. For detailed instructions, please refer to Section 34.7.
```