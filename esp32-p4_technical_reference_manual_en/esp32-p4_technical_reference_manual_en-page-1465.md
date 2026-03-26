

```markdown
Chapter 27 HMAC Accelerator (HMAC)

Write a correct purpose to register HMAC_SET_PARA_PURPOSE_REG (see Section 27.2.5). Note that the purpose of the key has also been programmed to eFuse memory. Only when the configured HMAC purpose matches the defined purpose of KEYn, the HMAC module will execute the configured calculation. Otherwise, it will return a matching error and stop the current calculation.

For example, suppose a user selects KEY3 for HMAC calculation, and the value programmed to EFUSE_KEY_PURPOSE_3 is 6 (EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG). Based on Table 27.2-1, KEY3 can be used to re-enable JTAG. If the value written to register HMAC_SET_PARA_PURPOSE_REG is also 6, then the HMAC module will start the process to re-enable JTAG.

Select Key from Key Manager

Users can deploy the HMAC key in the Key Manager. For deployment procedures, please refer to Section 34 Key Manager. To select this key from the Key Manager, write the key index 7 to the register HMAC_SET_PARA_KEY_REG. When a key is selected from the Key Manager, the intended operation target in the register is automatically set to "HMAC Calculation", and all other configurations will be ignored.

27.2.5 HMAC Process (Detailed)

The process for users to call HMAC in ESP32-P4 is as follows:

27.2.5.1 Enable HMAC Module

1. Set the peripheral clock bits for HMAC and SHA peripherals in register HP_SYS_CLKRST_REG_CRYPT_HMAC_CLK_EN, and clear the corresponding peripheral reset bits in register HP_SYS_CLKRST_REG_RST_EN_HMAC. For information on those registers, please see Chapter 10 Reset and Clock.

2. Write 1 to register HMAC_SET_START_REG.

27.2.5.2 Configure HMAC Keys and Key Purposes

1. Write the key purpose m to register HMAC_SET_PARA_PURPOSE_REG. The possible key purpose values are shown in Table 27.2-1. For more information, please refer to Section 27.2.4.

2. Select KEYn in eFuse memory as the key by writing n (ranges from 0 to 5, and 7) to register HMAC_SET_PARA_KEY_REG. For more information, please refer to Section 27.2.4.

3. Write 1 to register HMAC_SET_PARA_FINISH_REG to complete the configuration.

4. Read register HMAC_QUERY_ERROR_REG. If its value is 1, it means the purpose of the selected block does not match the configured key purpose and the calculation will not proceed. If its value is 0, it means the purpose of the selected block matches the configured key purpose, and then the calculation can proceed.

5. When the value of HMAC_SET_PARA_PURPOSE_REG is not 8, it means the HMAC module is in downstream mode, proceed with 27.2.5.3. When the value is 8, it means the HMAC module is in upstream mode, proceed with 27.2.5.4.

27.2.5.3 Downstream Mode Process

1. Poll Status register HMAC_QUERY_BUSY_REG until it reads 0.
```