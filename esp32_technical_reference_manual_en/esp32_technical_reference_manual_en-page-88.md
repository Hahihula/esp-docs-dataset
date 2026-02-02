**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Title:**
Table 4.3-18. MMU Entry Numbers for External RAM

| VAddr | Count | First MMU entry for PID |
|-------|-------|-------------------------|
|       | 0/1   |                         |
| LVAaddr_RAM | 128 | 1152, 1280, 1408, 1536, 1664, 1792, 1920 |
| RVAaddr_RAM | 128 | 3200, 3328, 3456, 3584, 3712, 3840, 3968 |

**Examples Section:**

- **Example 1. A PRO_CPU process**, with a PID of 7:
  - Needs to read or write external RAM address `0x7F_A375` via virtual address `0x3FA7_2375`. The MMU is in Low-High mode.
    - According to Table 4.3-9, the physical address `0x3FA7_2375` resides in the `0x4E'th` (32-KB-page of VAddr_RAM).
    - According to Table 4.3-16, virtual address `0x3FA7_2375` is governed by RVAaddr_RAM.
    - According to Table 4.3-18, the MMU entry for RVAaddr_RAM for PID 7 in the PRO_CPU starts at `3968`.
    - The modified MMU entry is `3968 + 0x4E = 4046`.
    - Address `0x7F_A375` resides in a `25th` (32-KB-sized page).
    - MMU entry for address `0x4E` needs to be set as valid by clearing the eighth bit. Thus, `0xFF` is written to MMU entry at physical address `0x4E`.
  
- **Example 2. An APP_CPU process**, with a PID of 5:
  - Needs to read or write external RAM address `0x55_5805` up to `0x55_5823` starting from virtual address `0x3F85_L805`.
    - The MMU is in Even-Odd mode.
    - According to Table 4.3-9, the physical address `0x3F85_L805` resides on the `0xA'th` (32-KB-page of VAddr_RAM).
    - Address range from `0x3F85_L805` is a span between two addresses in RVAaddr_RAM and LVAaddr_RAM.
    - According to Table 4.3-17, the MMU entry for LVAaddr_RAM for PID 5 starts at `1664`.
    - The modified MMU entries are `1664 + 0xOA = 1674` and `3712 + 0xOA = 3722`.
    - Addresses in the range from `0x55_5805` to `0x55_5823` reside on an `0xA'th` (32-KB-sized page).
    - MMU entries for addresses need setting as valid by clearing eighth bit. Thus, `0x0A` is written in the MMU entry at physical address `1674` and `3722`.
  
- **Example 3. A PRO_CPU process**, with a PID of 1:
  - Needs to read or write external RAM using virtual addresses from `0x3F80_0876`.
    - The PRO_CPU needs this region for accessing physical address at `0x10_0876`, while the APP_CPU wants access through an additional memory.
    - MMU is in Normal mode:
      - According to Table 4.3-9, virtual addresses from `0x10_0876` resides on a page of VAddr_RAM starting at address `1152`.
      - The modified entry for PID 1 starts as valid by clearing the eighth bit.
      - MMU entries are set to be written in memory with values: `1152 + 0 = 1152` and `3200 + 0 = 3200`.
  
- **Example Summary**:
  - For PRO_CPU, entry for PID is modified as valid by clearing the eighth bit.
    - Thus, address at physical memory location starts from virtual addresses.

**Footer:**
Espressif Systems
Page number and document version information (88 ESP32 TRM [Version 5.6])