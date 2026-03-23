

```markdown
## 21.2.4 HMAC eFuse Configuration

Each HMAC key burned into an eFuse block has a key purpose, specifying for which functionality the key can be used. The HMAC module will not accept a key with a non-matching purpose for any functionality. The HMAC module provides three different functionalities: re-enabling JTAG, DS KDF in downstream mode, and pure HMAC calculation in upstream mode. For each functionality, there exists a corresponding key purpose, listed in Table 21.2-1. Additionally, another purpose specifies a key which may be used for re-enabling JTAG as well as for serving as DS KDF.

Before enabling HMAC to do calculations, user should make sure the key to be used has been burned in eFuse by reading the registers EFUSE_KEY_PURPOSE_x (We totally have 6 keys in eFuse, so the value of x is 0 ~ 5) from 6 eFuse Controller. Take upstream mode as example, if there is no EFUSE_KEY_PURPOSE_HMAC_UP in EFUSE_KEY_PURPOSE_0 ~ 5, it means there is no upstream used key in eFuse. Users can burn key to eFuse as follows:

1. Prepare a secret 256-bit HMAC key and burn the key to an empty eFuse block y. As there are 6 blocks for storing a key in eFuse and the numbers of those blocks range from 4 to 9, the value of y is 4 ~ 9. Hence, when talking about key0, it means eFuse block4. Then, program the purpose to EFUSE_KEY_PURPOSE_(y – 4). Take upstream mode as an example: after programming the key, the user should program EFUSE_KEY_PURPOSE_HMAC_UP (corresponding value is 6) to EFUSE_KEY_PURPOSE_(y – 4). Please see Chapter 6 eFuse Controller on how to program eFuse keys.

2. Configure this eFuse key block to be read protected, so that users cannot read its value. A copy of this key should be kept by any party who needs to verify this device.

Please note that the key whose purpose is EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL can be used for both re-enabling JTAG or DS.

Table 21.2-1. HMAC Purposes and Configuration Value

| Purpose             | Mode       | Value | Description                                                                 |
|---------------------|------------|-------|-----------------------------------------------------------------------------|
| JTAG Re-enable      | Downstream | 6     | EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG                                            |
| DS KDF              | Downstream | 7     | EFUSE_KEY_PURPOSE_HMAC_DOWN_DIGITAL_SIGNATURE                               |
| HMAC Calculation    | Upstream   | 8     | EFUSE_KEY_PURPOSE_HMAC_UP                                                    |
| Both JTAG Re-enable and DS KDF | Downstream | 5     | EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL                                              |

### Configure HMAC Purposes

The correct purpose has to be written to register HMAC_SET_PARA_PURPOSE_REG (see Section 21.2.5). If there is no valid value in eFuse purpose section, HMAC will terminate calculation.

### Select eFuse Key Blocks

The eFuse controller provides six key blocks, i.e., KEY0 ~ 5. To select a particular KEYn for an HMAC calculation, write the key number n to register HMAC_SET_PARA_KEY_REG.
```