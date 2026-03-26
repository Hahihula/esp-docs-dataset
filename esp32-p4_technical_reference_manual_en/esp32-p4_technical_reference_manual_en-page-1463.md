

```markdown
2. Write the correctly padded message to the HMAC, one block at a time.
3. Read back the result from HMAC.

For details of this process, please see Section 27.2.5.

Note:
Common use cases for the upstream mode are challenge-response protocols supporting HMAC-SHA-256. Assume
the two entities in the challenge-response protocol are A and B respectively, and the data message they expect to
exchange is M. The general authentication process of this protocol is as follows:

*   A calculates a unique random number M.
*   A sends M to B.
*   B calculates the HMAC (through M and KEY) and sends the result to A.
*   A calculates the HMAC (through M and KEY) internally.
*   A compares the two results. If the results are the same, then the identity of B is authenticated.

27.2.2 Downstream Mode - JTAG Enable Feature

JTAG debugging can be disabled by eFuse in a way which allows later re-enabling using the HMAC module.
(For more details, please see Chapter 8 eFuse Controller (EFUSE).) The HMAC module will expect the user to
supply the HMAC result for one of the eFuse keys. The HMAC module will check whether the supplied HMAC
matches the one calculated from the chosen key. If both HMACs are the same, JTAG will be enabled until the
user calls the HMAC module to clear the results and consequently disable JTAG again.

To re-enable JTAG, users should perform the following steps:

1.  Enable the HMAC module by initializing clock and reset signals of HMAC, and enter downstream JTAG
    enable mode by configuring HMAC_SET_PARA_PURPOSE_REG. Then, wait for the calculation to complete.
    Please see Section 27.2.5 for more details.

2.  Write 1 to the HMAC_SOFT_JTAG_CTRL_REG register to enter JTAG re-enable mode.

3.  Write the 256-bit HMAC value to register HMAC_WR_JTAG_REG. This value is obtained by performing a
    local HMAC calculation from the 32-byte 0x00 using SHA-256 and the key that has been written to the
    eFuse. It needs to be written 8 times and 32-bit each time in big-endian word order.

4.  If the HMAC result calculated from the key in the eFuse matches the value that users wrote in step 3,
    then JTAG is re-enabled. Otherwise, JTAG remains disabled.

5.  After writing 1 to HMAC_SET_INVALIDATE_JTAG_REG or resetting the chip, JTAG will be disabled. If users
    want to re-enable JTAG again, they need to repeat the above steps again.

27.2.3 Downstream Mode - RSA_DS Key Derivation Feature

The RSA Digital Signature Peripheral (RSA_DS) encrypts its parameters using the AES-CBC algorithm. The
HMAC module is used as a Key Derivation Function (KDF) to derive the AES key to decrypt these parameters
(parameter decryption key).

Before starting the RSA_DS peripheral, users need to obtain the parameter decryption key for the RSA_DS
peripheral through HMAC calculation. For more information, please see Chapter 30 RSA Digital Signature
```