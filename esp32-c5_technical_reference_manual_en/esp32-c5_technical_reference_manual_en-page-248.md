

```markdown
Chapter 7

eFuse Controller (EFUSE)

7.1 Overview

ESP32-C5 contains a 4096-bit eFuse memory to store parameters and user data. The parameters include control parameters for some hardware modules, system data parameters and keys used for the encryption/decryption module. Once an eFuse bit is programmed to 1, it can never be reverted to 0. The eFuse controller programs bits in eFuse according to user configurations. From outside the chip, eFuse data can only be read via the eFuse controller. For some data, such as some keys stored in eFuse for internal use by hardware cryptography modules (e.g., digital signature, HMAC), if read protection is not enabled, the data can be read from outside the chip; if read protection is enabled, the data cannot be read from outside the chip.

7.2 Features

- 4096-bit one-time programmable memory (including up to 1792 bits reserved for custom use; depending on whether the EFUSE_KEY_PURPOSE_n parameters are set to 0. For more information, see Table 7.3-2.)
- Configurable write protection
- Configurable read protection
- Various hardware encoding schemes against data corruption

7.3 Functional Description

7.3.1 Structure

The eFuse system consists of the eFuse controller and eFuse memory. Data flow in this system is shown in Figure 7.3-1.

Users can program bits in the eFuse memory via the eFuse controller by writing the data to the programming register and executing the programming instruction. For detailed programming steps, please refer to Section 7.3.2.

Users cannot directly read the data programmed in the eFuse memory, so they need to read the programmed data into the Reading Data Register of the corresponding address segment through the eFuse controller. During the reading process, if the data is inconsistent with that in the eFuse memory, the eFuse controller can automatically correct it through the hardware encoding mechanism (see Section 7.3.1.3 for details), and send the error message to the error report register. For detailed steps to read parameters, please refer to the Section 7.3.3.
```