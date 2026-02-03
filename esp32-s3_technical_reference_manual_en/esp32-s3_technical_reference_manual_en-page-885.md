**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**Table Header:**
Table 21.2-1. HMAC Purposes and Configuration Values

| Purpose | Mode | Value |
|---------|------|-------|
| JTAG Re-enable | Downstream | 6 EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG |
| DS Key Derivation | Downstream | 7 EFUSE_KEY PURPOSE HMAC DOWN DIGITAL SIGNATURE |
| HMAC Calculation | Upsstream | 8 EFUSE_KEY PURPOSE HMAC UP |
| Both JTAG Re-enable and DS KDF | Downstream | 5 EFUSE_KEY PURPOSE HMAC DOWN ALL |

**Body Text:**
Before enabling HMAC to do calculations, user should make sure the key to be used has been burned in eFuse. You can burn a key to eFuse as follows:

1. Prepare a secret 256-bit HMAC key and burn the key to an empty eFuse block y (there are six blocks for storing a key in eFuse). The numbers of those blocks range from 4 to 9, so y = 4,5,...,9. Hence, if we are talking about key0, we mean an eFuse block4), and then program the purpose to EFUSE_KEY PURPOSE (y – 4). Take upstream mode as an example: after programming the key, the user should program EFUSE_KEY PURPOSE_HMAC UP (corresponding value is 8) to EFUSE_KEY PURPOSE (y – 4). Please see Chapter 5 eFuse Controller on how to program eFuse keys.

2. Configure this eFuse key block to be read protected, so that users cannot read its value. A copy of this key should be kept by any party who needs to verify this device.

**Subsection Title:**
21.2.5 HMAC Initialization

The eFuse key blocks (with correctly programmed purpose values) must be coordinated with the HMAC modes, or HMAC will terminate calculation.

- **Configure HMAC modes**

  The correct purpose (see Table 21.2-1) has to be written to register HMAC_SET_PARA PURPOSE REG by the user.
  
- **Select eFuse Key Blocks**

  The eFuse controller provides six key blocks, i.e., KEYO ~ 5. To select a particular KEYn for a certain HMAC calculation, write the key number n to register HMAC SET PARA KEY REG.

Note that the purpose of the key has also been programmed to eFuse memory. Only when the configured HMAC purpose matches the defined purpose of KEYn, will the HMAC module execute the configured calculation. Otherwise, it will return a matching error and stop the current calculation. For example, suppose a user selects KEY3 for HMAC calculation, and the value programmed to KEY PURPOSE_3 is 6 (EFUSE_KEY PURPOSE_HMAC DOWN JTAG). Based on Table 21.2-1, KEY3 can be used to re-enable JTAG. If the value written to register HMAC SET PARA PURPOSE REG is also 6, then the HMAC module will start the process to re-enable JTAG.

**Subsection Title:**
21.2.6 HMAC Process (Detailed)

The process to call HMAC in ESP32-S3 is as follows:

1. Enable HMAC module

**Footer Information:**
Espressif Systems
885
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback