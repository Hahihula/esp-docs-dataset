

```markdown
| Bus Type         | Boundary Address                     | Size   | Target*     |
|------------------|---------------------------------------|--------|-------------|
|                  | Low Address     | High Address |        |
| Data/Instruction bus | 0x3010_0000    | 0x3010_1FFF | 8 KB       | HP SPM      |
|                  | 0x3010_2000    | 0x3FEF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x3F0_0000     | 0x3FF1_FFFF | 128 KB    | HP CPU peripherals |
|                  | 0x3F2_0000     | 0x3FFF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x4000_0000    | 0x43FF_FFFF | 64 MB     | External flash |
|                  | 0x4400_0000    | 0x47FF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x4800_0000    | 0x4BFF_FFFF | 64 MB     | External RAM |
|                  | 0x4C00_0000    | 0x4FBF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x4FC0_0000    | 0x4FC1_FFFF | 128 KB    | HP ROM      |
|                  | 0x4FC2_0000    | 0x4FEF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x4FF0_0000    | 0x4FFB_FFFF | 768 KB    | HP L2MEM    |
|                  | 0x4FFC_0000    | 0x4FFF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x5000_0000    | 0x500F_FFFF | 1 MB      | HP peripherals |
| Data/Instruction bus | 0x5010_0000    | 0x5010_3FFF | 16 KB     | LP ROM      |
|                  | 0x5010_4000    | 0x5010_7FFF | Reserved   |             |
| Data/Instruction bus | 0x5010_8000    | 0x5010_FFFF | 32 KB     | LP SRAM     |
| Data/Instruction bus | 0x5011_0000    | 0x5012_FFFF | 128 KB    | LP peripherals |
|                  | 0x5013_0000    | 0x7FFF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x8000_0000     | 0x83FF_FFFF | 64 MB     | External flash (direct access by CPU) |
|                  | 0x8400_0000     | 0x87FF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x8800_0000     | 0x8BFF_FFFF | 64 MB     | External RAM (direct access by CPU) |
|                  | 0x8C00_0000     | 0x8FBF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x8FC0_0000     | 0x8FC1_FFFF | 128 KB    | HP ROM (direct access by CPU) |
|                  | 0x8FC2_0000     | 0x8FEF_FFFF | Reserved   |             |
| Data/Instruction bus | 0x8FF0_0000     | 0x8FFB_FFFF | 768 KB    | HP L2MEM (direct access by CPU) |
|                  | 0x8FFC_0000     | 0xFFFF_FFFF | Reserved   |             |

\* Address starting with 0x4xxx_xxxx can be configured as noncache-able or cache-able, depending on CPU PMA, whereas address starting with 0x8xxx_xxxx is accessed directly by CPU.
\* For the targets accessible by HP CPU or LP CPU, see Figure 7.3-1.
```

## 7.3.2 Internal Memory

ESP32-P4 has various types of internal memory:

*   **HP ROM (128 KB):** This read-only memory is dedicated to the HP system and is not programmable. It contains the ROM code and read-only data of some low-level system software. The HP ROM is accessed by the HP CPU through the I2 cache at half the frequency of HP CPU.
*   **HP L2MEM (768 KB):** A volatile memory accessible by the HP CPU, LP CPU, or DMA peripherals at half the frequency of the HP CPU. HP L2MEM can be configured to retain power during Light-sleep mode, making it suitable for data retention or register backup.
*   **LP ROM (16 KB):** This read-only memory serves the LP system, containing the code for booting the LP CPU and some basic system functions. The LP ROM is accessed by the LP CPU with zero latency.
```