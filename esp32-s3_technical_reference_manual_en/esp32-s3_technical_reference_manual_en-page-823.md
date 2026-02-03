**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Body Text:**

- **In register SYSCON_MEM_POWER_DOWN_REG:**  
  - Setting different bits of the SYSCON_ROM_POWER_DOWN field sends different blocks of Internal ROM 0 and Internal ROM 1 into retention state.
  - Setting different bits of the SYSCON_SRAM_POWER_DOWN field sends different blocks of Internal SRAM into retention state.
  - The “Retention” state is a low-power state of a memory block. In this state, the memory block still holds all the data stored but cannot be accessed, thus reducing the power consumption. Therefore, you can set a certain block of memory into the retention state to reduce power consumption if you know are not going to use such memory block for some time.

- **In register SYSCON_MEM_POWER_UP_REG:**  
  - By default, all memory enters low-power state when the chip enters Light-sleep mode.
  - Setting different bits of the SYSCON_ROM_POWER_UP field forces different blocks of Internal ROM 0 and Internal ROM 1 to work as normal (do not enter retention state) when the chip enters Light-sleep.

- **Setting different bits of the SYSCON_SRAM_POWER_UP field**  
  - For detailed information about controlling bits of different memory, please see Table 17.3-1 below.
  - Setting different blocks to work as normal (do not enter retention state) when the chip enters Light-sleep.

**Table Title:**
Table 17.3-1. Internal Memory Controlling Bit

| Internal Memory | Lowest Address1       | Highest Address1      | Lowest Address2   | Highest Address2    | Controlling Bit |
|-----------------|------------------------|-----------------------|-------------------|---------------------|-----------------|
| Internal ROM 0 | 0x4000_0000           | 0x4003_FFFF           | -                 | -                   | BitO             |
| Internal ROM 1 | 0x4004_0000           | 0x4004_FFFF           | -                 | -                   | Bit1             |
| Internal ROM 2 | 0x4005_0000           | 0x4005_FFFF           | 0x3FF0_0000       | OX3FF0_FFFF         | Bit2             |
| SRAM Block0    | 0x4037_0000           | 0x4037_3FFF           | -                 | -                   | BitO             |
| SRAM Block1    | 0x4037_4000           | 0x4037_FFFF           | -                 | -                   | Bit1             |
| SRAM Block2    | 0x4037_8000           | 0x4037_FFFF           | OX3FC8_8000       | Ox3EC8_FFFF         | Bit2             |
| SRAM Block3    | 0x4038_0000           | 0x4038_FFFF           | 0x3FC9_0000       | OX3FC9_FFFF         | Bit3             |
| SRAM Block4    | 0x4039_8000           | 0x4039_FFFF           | 0x3FCA_0000       | Ox3FCA_FFFF         | Bit4             |
| SRAM Block5    | 0x403A_C000           | 0x403A_FFFF           | OX3FCB_C000       | Ox3FCB_FFFF         | Bit5             |
| SRAM Block6    | 0x403B_0000           | 0x403B_FFFF           | -                 | -                   | Bit6             |
| SRAM Block7    | 0x403C_0000           | 0x403C_FFFF           | OX3FCD_4000       | Ox3FCD_FFFF         | Bit7             |
| SRAM Block8    | 0x403D_0000           | 0x403D_BFFF           | -                 | -                   | Bit8             |
| SRAM Block9    | -                      | -                     | OX3FCF_0000       | Ox3FCF_7FFF         | Bit9             |
| SRAM Block10   | -                      | -                     | 0x3FCF_8000       | Ox3FCF_FFFF         | Bit10            |

**Footer:**
For detailed information about the controlling bits of different blocks, please see Table 17.3-1 below.

**Page Footer Information:**  
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)  
823