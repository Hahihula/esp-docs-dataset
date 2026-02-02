**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Header:**
- Peripheral
- Authority

| Peripheral | PID = 0/1 | PID = 2 ~ 7 |
|------------|-----------|-------------|
| SYSCON     | Access    | DPORT_AHBLITE_MPU_TABLE_APB_CTRL_REG |
| I2C1       | Access    | DPORT_AHBLITE_MPU_TABLE_I2C_EXT1_REG |
| SDMMC      | Access    | DPORT_AHBLITE_MPU_TABLE_SDIO_HOST_REG |
| EMAC       | Access    | DPORT_AHBLITE_MPU_TABLE_EMAC_REG |
| PWM1       | Access    | DPORT_AHBLITE_MPU_TABLE_PWM1_REG |
| I2S1       | Access    | DPORT_AHBLITE_MPU_TABLE_I2S1_REG |
| UART2      | Access    | DPORT_AHBLITE_MPU_TABLE_UART2_REG |
| RNG        | Access    | DPORT_AHBLITE_MPU_TABLE_PWR_REG |

**Body Text:**
Each bit of register DPOR_AHBLITE_MPU_TABLE_X_REG determines whether each process can access the peripherals managed by the register. For details please see Table 4.3-20.

**Table Reference and Description (Table 4.3-20):**
DPORT_AHBLITE_MPU_TABLE_X_REG

| PID | DPORT_AHBLITE_MPU_TABLE_X_REG bit |
|-----|----------------------------------|
| 1   | O                                |
| 2   | I                                |
| 3   | C                                |
| 4   | B                                |
| 5   | A                                |
| 6   | L                                |
| 7   | T                                |

**Additional Information:**
All the DPORT_AHBLITE_MPU_TABLE_X_REG registers are in peripheral DPort Register. Only processes with PID 0/1 can modify these registers.

**Footer:**
Espressif Systems
90 ESP32 TRM (Version 5.6)
Submit Documentation Feedback