

```markdown
- A compares the two results. If the results are the same, then the identity of B is authenticated.

To calculate the HMAC value, users should perform the following steps:

1. Initialize the HMAC module, and enter upstream mode.
2. Write the correctly padded message to the HMAC, one block at a time.
3. Read back the result from HMAC.

For details of this process, please see Section 21.2.5.

## 21.2.2 Downstream JTAG Enable Mode

JTAG debugging can be disabled in a way which allows later re-enabling using the HMAC module. The HMAC module will expect the user to supply the HMAC result for one of the eFuse keys. The HMAC module will check whether the supplied HMAC matches the one calculated from the chosen key. If both HMACs are the same, JTAG will be enabled until the user calls the HMAC module to clear the results and consequently disable JTAG again.

There are two parameters in eFuse memory to disable JTAG: `EFUSE_DIS_PAD_JTAG` and `EFUSE_SOFT_DIS_JTAG`. Write 1 to `EFUSE_DIS_PAD_JTAG` to disable JTAG permanently, and write odd numbers of 1 to `EFUSE_SOFT_DIS_JTAG` to disable JTAG temporarily. For more details, please see Chapter 6 eFuse Controller. After bit `EFUSE_SOFT_DIS_JTAG` is set, the key to re-enable JTAG can be calculated in HMAC module’s downstream mode. JTAG is re-enabled when the result configured by the user is the same as the HMAC result.

To re-enable JTAG, users should perform the following steps:

1. Enable the HMAC module by initializing clock and reset signals of HMAC, and enter downstream JTAG enable mode by configuring `HMAC_SET_PARA_PURPOSE_REG`. Then, wait for the calculation to complete. Please see Section 21.2.5 for more details.
2. Write 1 to the `HMAC_SOFT_JTAG_CTRL_REG` register to enter JTAG re-enable compare mode.
3. Write the 256-bit HMAC value to register `HMAC_WR_JTAG_REG`. This value is obtained by preforming a local HMAC calculation from the 32-byte 0x00 using SHA-256 and the generated key. It needs to be written by 8 times and 32-bit each time in big-endian word order.
4. If the HMAC result matches the value that users calculated locally, then JTAG is re-enabled. Otherwise, JTAG remains disabled.
5. After writing 1 to `HMAC_SET_INVALIDATE_JTAG_REG` or resetting the chip, JTAG will be disabled. If users want to re-enable JTAG again, please repeat the above steps again.

## 21.2.3 Downstream Digital Signature Mode

The Digital Signature (DS) module encrypts its parameters using the AES-CBC algorithm. The HMAC module is used as a Key Derivation Function (KDF) to derive the AES key to decrypt these parameters (parameter decryption key). The key used for the HMAC as KDF is stored in one of the eFuse key blocks.

Before starting the DS module, users need to obtain the parameter decryption key for the DS module through HMAC calculation. For more information, please see Chapter 24 Digital Signature (DS). After the chip is powered on, the HMAC module will check whether the key required to calculate the parameter decryption key
```