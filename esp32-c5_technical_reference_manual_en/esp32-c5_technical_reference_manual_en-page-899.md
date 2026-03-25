

```markdown
| Purpose(m)               | Mode     | Value | Description                                                                 |
|--------------------------|----------|-------|-----------------------------------------------------------------------------|
| JTAG Re-enable           | Downstream| 6     | EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG                                            |
| DSA KDF                  | Downstream| 7     | EFUSE_KEY_PURPOSE_HMAC_DOWN_DIGITAL_SIGNATURE                               |
| HMAC Calculation         | Upstream  | 8     | EFUSE_KEY_PURPOSE_HMAC_UP                                                    |
| Both JTAG Re-enable and DSA KDF | Downstream| 5     | EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL                                             |

## Select eFuse Key Blocks and HMAC Purposes

The eFuse controller provides six key blocks, i.e., KEY0 ~ 5. To select a particular KEYn for an HMAC calculation, write the key number n to register HMAC_SET_PARA_KEY_REG.

Write a correct purpose to register HMAC_SET_PARA_PURPOSE_REG (see Section 24.5). Note that the purpose of the key has also been programmed to eFuse memory. Only when the configured HMAC purpose matches the defined purpose of KEYn, the HMAC module will execute the configured calculation. Otherwise, it will return a matching error and stop the current calculation.

For example, suppose a user selects KEY3 for HMAC calculation, and the value programmed to EFUSE_KEY_PURPOSE_3 is 6 (EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG). Based on Table 24.4-1, KEY3 can be used to re-enable JTAG. If the value written to register HMAC_SET_PARA_PURPOSE_REG is also 6, then the HMAC module will start the process to re-enable JTAG.

## Select the Key from the Key Manager

Users can deploy the HMAC key in the key manager. To select this key from the key manager, write the key number 7 to register HMAC_SET_PARA_KEY_REG. When users choose the HMAC key from the key manager, the HMAC purpose will automatically be "HMAC Calculation", and any configuration to register HMAC_SET_PARA_PURPOSE_REG takes no effect.

## 24.5 HMAC Process (Detailed)

The process for users to call HMAC in ESP32-C5 is as follows:

### 24.5.1 Enable HMAC module

1. Set the peripheral clock bits for HMAC and SHA peripherals in register HP_SYS_CLKRST_REG_CRYPTO_HMAC_CLK_EN, and clear the corresponding peripheral reset bits in register HP_SYS_CLKRST_REG_RST_EN_HMAC. For information on those registers, please see Chapter 9 Reset and Clock.
2. Write 1 to register HMAC_SET_START_REG.

### 24.5.2 Configure HMAC keys and key purposes

1. Write the key purpose m to register HMAC_SET_PARA_PURPOSE_REG. The possible key purpose values are shown in Table 24.4-1. For more information, please refer to Section 24.4.
2. Select KEYn in eFuse memory as the key by writing n (ranges from 0 to 5, and 7) to register
```