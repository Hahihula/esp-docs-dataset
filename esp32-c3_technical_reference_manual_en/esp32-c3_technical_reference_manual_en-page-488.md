

```markdown
has been burned in the eFuse block. If the key has been burned, HMAC module will automatically enter the downstream digital signature mode and complete the HMAC calculation based on the chosen key.

## 19.2.4 HMAC eFuse Configuration

Each HMAC key burned into an eFuse block has a key purpose, also burned into the eFuse section. This purpose specifies for which functionality the key can be used. The HMAC module will not accept a key with a non-matching purpose for any functionality. The HMAC module provides three different functionalities: re-enabling JTAG and serving as DS KDF in downstream mode as well as pure HMAC calculation in upstream mode. For each functionality, there exists a corresponding key purpose, listed in Table 19.2-1. Additionally, another purpose specifies a key which may be used for re-enabling JTAG as well as for serving as DS KDF.

Before enabling HMAC to do calculations, user should make sure the key to be used has been burned in eFuse by reading EFUSE_KEY_PURPOSE_X (We totally have 6 keys in eFuse, so x = 0,1,2,...5), registers from 4 eFuse Controller (EFUSE). Take upstream as example, if there is no EFUSE_KEY_PURPOSE_HMAC_UP in EFUSE_KEY_PURPOSE_0~5, means there is no upstream used key in efuse. You can burn key to efuse as follows:

1. Prepare a secret 256-bit HMAC key and burn the key to an empty eFuse block y (there are six blocks for storing a key in eFuse. The numbers of those blocks range from 4 to 9, so y = 4,5,...,9. Hence, if we are talking about key0, we mean eFuse block4), and then program the purpose to EFUSE_KEY_PURPOSE_(y – 4). Take upstream mode as an example: after programming the key, the user should program EFUSE_KEY_PURPOSE_HMAC_UP (corresponding value is 6) to EFUSE_KEY_PURPOSE_(y – 4). Please see Chapter 4 eFuse Controller (EFUSE) on how to program eFuse keys.

2. Configure this eFuse key block to be read protected, so that users cannot read its value. A copy of this key should be kept by any party who needs to verify this device.

Please note that the key whose purpose is EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL can be used for both re-enabling JTAG or DS.

Table 19.2-1. HMAC Purposes and Configuration Value

| Purpose             | Mode       | Value | Description                                                                 |
|---------------------|------------|-------|-----------------------------------------------------------------------------|
| JTAG Re-enable      | Downstream | 6     | EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG                                            |
| DS Key Derivation    | Downstream | 7     | EFUSE_KEY_PURPOSE_HMAC_DOWN_DIGITAL_SIGNATURE                               |
| HMAC Calculation     | Upstream   | 8     | EFUSE_KEY_PURPOSE_HMAC_UP                                                   |
| Both JTAG Re-enable and DS KDF | Downstream | 5     | EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL                                             |

Configure HMAC Purposes

The correct purpose has to be written to register HMAC_SET_PARA_PURPOSE_REG (see Section 19.2.5). If there is no valid value in efuse purpose section, HMAC will terminate calculation.

Select eFuse Key Blocks

The eFuse controller provides six key blocks, i.e., KEY0 ~ 5. To select a particular KEYn for an HMAC calculation, write the key number n to register HMAC_SET_PARA_KEY_REG.
```