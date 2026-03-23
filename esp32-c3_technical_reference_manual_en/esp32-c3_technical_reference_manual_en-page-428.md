

```markdown
| Memory          | Lowest Address1 | Highest Address1 | Lowest Address2 | Highest Address2 | Controlling Bit |
|-----------------|-----------------|------------------|-----------------|------------------|-----------------|
| ROM 0           | 0x4000_0000     | 0x4003_FFFF      | -               | -                | Bit0            |
| ROM 1           | 0x4004_0000     | 0x4005_FFFF      | 0x3FF0_0000     | 0x3FF1_FFFF      | Bit1            |
| SRAM Block 0    | 0x4037_C000     | 0x4037_FFFF      | -               | -                | Bit0            |
| SRAM Block 1    | 0x4038_0000     | 0x4039_FFFF      | 0x3FC8_0000     | 0x3FC9_FFFF      | Bit1            |
| SRAM Block 2    | 0x403A_0000     | 0x403B_FFFF      | 0x3FCA_0000     | 0x3FCB_FFFF      | Bit2            |
| SRAM Block 3    | 0x403C_0000     | 0x403D_FFFF      | 0x3FCC_0000     | 0x3FCD_FFFF      | Bit3            |
```
```markdown
## Chapter 16 System Registers (SYSREG)
GoBack

automatically when the corresponding ROM or SRAM blocks are not accessed. Therefore, it's recommended to configure these bits to 0 to lower power consumption.

* In register `SYSCON_MEM_POWER_DOWN_REG`:
    - Setting different bits of the `SYSCON_ROM_POWER_DOWN` field sends different blocks of Internal ROM 0 and Internal ROM 1 into retention state.
    - Setting different bits of the `SYSCON_SRAM_POWER_DOWN` field sends different blocks of Internal SRAM into retention state.
    - The "Retention" state is a low-power state of a memory block. In this state, the memory block still holds all the data stored but cannot be accessed, thus reducing the power consumption. Therefore, you can send a certain block of memory into the retention state to reduce power consumption if you know you are not going to use such memory block for some time.
* In register `SYSCON_MEM_POWER_UP_REG`:
    - By default, all memory enters low-power state when the chip enters the Light-sleep mode.
    - Setting different bits of the `SYSCON_ROM_POWER_UP` field forces different blocks of Internal ROM 0 and Internal ROM 1 to work as normal (do not enter the retention state) when the chip enters Light-sleep.
    - Setting different bits of the `SYSCON_SRAM_POWER_UP` field forces different blocks of Internal SRAM to work as normal (do not enter the retention state) when the chip enters Light-sleep.

For detailed information about the controlling bits of different blocks, please see Table 16.3-1 below.

Table 16.3-1. Memory Controlling Bit

| Memory          | Lowest Address1 | Highest Address1 | Lowest Address2 | Highest Address2 | Controlling Bit |
|-----------------|-----------------|------------------|-----------------|------------------|-----------------|
| ROM 0           | 0x4000_0000     | 0x4003_FFFF      | -               | -                | Bit0            |
| ROM 1           | 0x4004_0000     | 0x4005_FFFF      | 0x3FF0_0000     | 0x3FF1_FFFF      | Bit1            |
| SRAM Block 0    | 0x4037_C000     | 0x4037_FFFF      | -               | -                | Bit0            |
| SRAM Block 1    | 0x4038_0000     | 0x4039_FFFF      | 0x3FC8_0000     | 0x3FC9_FFFF      | Bit1            |
| SRAM Block 2    | 0x403A_0000     | 0x403B_FFFF      | 0x3FCA_0000     | 0x3FCB_FFFF      | Bit2            |
| SRAM Block 3    | 0x403C_0000     | 0x403D_FFFF      | 0x3FCC_0000     | 0x3FCD_FFFF      | Bit3            |

For more information, please refer to Chapter 3 System and Memory.

### 16.3.1.2 External Memory

`SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` configures encryption and decryption options of the external memory. For details, please refer to Chapter 23 External Memory Encryption and Decryption (XTS_AES).

### 16.3.1.3 RSA Memory

`SYSTEM_RSA_PD_CTRL_REG` controls the SRAM memory in the RSA accelerator.

* Setting the `SYSTEM_RSA_MEM_PD` bit to send the RSA memory into retention state. This bit has the lowest priority, meaning it can be masked by the `SYSTEM_RSA_MEM_FORCE_PU` field. This bit is invalid when the Digital Signature (DS) occupies the RSA.
```