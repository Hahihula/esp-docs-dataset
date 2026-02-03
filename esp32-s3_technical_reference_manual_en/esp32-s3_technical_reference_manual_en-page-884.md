**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**Body Text with List and Steps:**

- B calculates the HMAC value through M and KEY) and sends the result to A.
- Also calculates the HMAC value internally.

A compares these two values. If they are same, then identity of B is authenticated

To calculate the HMAC value:
1. Initialize the HMAC module, and enter upstream mode
2. Write correctly padded message to the HMAC one block at a time 
3. Read back result from HMAC.
For details about this process please see Section 21.2.6.

**Subtitle:**
21.2.2 Downstream JTAG Enable Mode

**Body Text with List and Steps:**

There are two parameters in the fuse memory to disable JTAG debugging, namely EFUSE_DIS_PAD_JTAG and EFUSE_SOFTDisJTAG. Set EFUSE_DIS_PAD_JTAG to 1 can disable JTAG permanently set odd numbers of 1 to EFUSE_SOFTDisJTAG can disable JTAG temporarily for more details please see Chapter eFuse Controller.

To re-enable the temporarily disabled JTAG, users follow these steps below:
1. Enable the HMAC module and enter downstream JTAG enable mode.
2. Write 1 to the HMACSOFTJCTRLREG register to enter JTAG re-enable compare mode
3. Write the 256-bit HMAC value which is calculated locally from the 32-byte OXOO using HMAC-SHA-256 algorithm pre-generated key to register HMACWRJTAGREG in big-endian order of word.
4. If the HMAC internally calculated value matches user programmed, then JTAG re-enabled otherwise JTAG remains disabled
5. JTAG remains status step until writer 1 to register HMACSINVALIDATEJCTRLREG or restart JTAG.

For detailed steps this process please see Section 21.2.6

**Subtitle:**
21.2.3 Downstream Digital Signature Mode

**Body Text with Explanation and Steps:**

The Digital Signature (DS) module encrypts its parameters using AES-CBC algorithm. The HMAC module is used as Key Derivation Function to derive the AES key for decrypt these parameters.

Before starting DS module, user needs obtain the key first through HMAC calculation more information please see Chapter 22 Digital Signature (DS). After clock of HMAC be enabled and reset of HMAC released, the HMAC module will check if there functional key in eFuses for the DS module. If yes, HMAC enter downstream digital signature mode finish DS key calculation automatically.

**Subtitle:**
21.2.4 HMAC eFuse Configuration

**Body Text with Explanation and Table Reference:**

The HMAC module provides three different functionalities re-enabling JTAG serving as DS KDF in downstream mode also upstream mode. Table 21.2-1 lists the register value corresponding to each purpose which should be written to register HMACSETPARAPURPOSE REG by user (see Section 21.2.6).

**Footer:**
Espressif Systems
884 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback