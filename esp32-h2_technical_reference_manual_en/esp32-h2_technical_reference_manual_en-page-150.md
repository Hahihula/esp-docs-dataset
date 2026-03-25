

# Chapter 5

## eFuse Controller (EFUSE)

### 5.1 Overview

ESP32-H2 contains a 4096-bit eFuse memory to store user data and hardware parameters, including control parameters for hardware modules, calibration parameters, the MAC address, and keys used for the encryption and decryption module. Once an eFuse bit is programmed to 1, it can never be reverted to 0. Users cannot directly access the eFuse memory. They can only use the eFuse controller to read and write eFuse memory bits. For confidential data in eFuse memory, read protection can be enabled by programming the corresponding read protection bit. So, the data cannot be accessed via the controller.

### 5.2 Features

*   4096-bit one-time-programmable memory including 1792 bits reserved for custom use
*   Configurable write protection
*   Configurable read protection
*   Various hardware encoding schemes against data corruption

### 5.3 Functional Description

#### 5.3.1 Structure

The eFuse system consists of the eFuse controller and eFuse memory. Data flow in this system is shown in Figure 5.3-1.

To program data to the eFuse memory, write the data to the programming register first and then execute the programming instruction. For detailed programming steps, please refer to Section 5.3.2.

Users cannot directly read data from the eFuse memory. They need to use the eFuse controller to take the data into the reading data register of the corresponding address segment. During the reading process, if the data is inconsistent with that in the eFuse memory, the eFuse controller can automatically correct it through the hardware encoding mechanism (see Section 5.3.1.4 for details), and send the error message to the error report register. For detailed steps to read parameters, please refer to Section 5.3.3.