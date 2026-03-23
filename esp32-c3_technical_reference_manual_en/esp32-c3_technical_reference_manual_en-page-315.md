

# Chapter 14

## Permission Control (PMS)

### 14.1 Overview

ESP32-C3 includes a Permission Controller (PMS), which allocates the hardware resources (memory and peripherals) to two isolated environments, thereby realizing the separation of privileged and unprivileged environments.

*   **Privileged Environment:**
    - Can access all peripherals and memories;
    - Performs all confidential operations, such as user authentication, secure communication, and data encryption and decryption, etc.
*   Unprivileged Environment:
    - Can access some peripherals and memories;
    - Performs other operations, such as user operation and different applications, etc.

Besides, ESP32-C3's RISC-V CPU also has a Physical Memory Protection (PMP) unit, which can be used by software to set memory access privileges (read, write, and execute permissions) for required memory regions. However, the PMP unit has some limitations:

*   Only supports up to 16 configurable PMP regions, which sometimes are not enough to fully support the access management requirement of ESP32-C3's rich peripherals and different types of memories.
*   Can only control CPU, not GDMA.

To this, ESP32-C3 has specially implemented this Permission Controller to complete the Physical Memory Protection unit.

ESP32-C3's completed workflow of permission check can be described below (also see Figure 14.1-1):

1.  Check PMP permission
    *   Pass: then continue and further check PMS permission
    *   Fail: throw an exception and will not further check PMS permission

2.  Check PMS permission
    *   Pass: access allowed
    *   Fail: trigger an interrupt