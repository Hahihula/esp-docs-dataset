

# Chapter 5
## eFuse Controller (EFUSE)

### 5.1 Overview

ESP32-C61 contains a 4096-bit eFuse memory to store parameters and user data. The parameters include control settings for some hardware modules, system data parameters, and keys used for the decryption module. Once an eFuse bit is programmed to 1, it can never be reverted to 0. The eFuse controller programs individual bits of parameters in eFuse according to user configurations. From outside the chip, eFuse data can only be read via the eFuse controller. For some data, such as some keys stored in eFuse for internal use by hardware cryptography modules (e.g., digital signature, HMAC), if read protection is not enabled, the data can be read from outside the chip; if read protection is enabled, the data cannot be read from outside the chip.

### 5.2 Feature List

*   4096-bit one-time programmable storage with 1792 reserved bits for users
*   Configurable write protection
*   Configurable read protection
*   Various hardware encoding schemes against data corruption

### 5.3 Architectural Overview

The eFuse system consists of the eFuse controller and eFuse memory. Data flow in this system is shown in Figure 5.3-1.

Users can program bits in the eFuse memory via the eFuse controller by writing the data to be programmed to the programming register and executing the programming instruction. For detailed steps, please refer to Section 5.4.1.

Users cannot directly read the data programmed in the eFuse memory, so they need to read the programmed data into the Reading Data Register of the corresponding address segment through the eFuse controller. During the reading process, if the data is inconsistent with that in the eFuse memory, the eFuse controller can automatically correct it through the hardware encoding mechanism (see Section 5.3.3 for details), and send the error message to the error report register. For detailed steps to read parameters, please refer to the Section 5.4.2.