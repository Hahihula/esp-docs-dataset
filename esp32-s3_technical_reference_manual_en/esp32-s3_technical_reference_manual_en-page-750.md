**Title:**
Register 15.41. PMS_CORE_X_IRAMO_PMS CONSTRAINT_1_REG (0x0ODC)

**Body Text with Table and Descriptions:**

| Register Address | Description |
|------------------|-------------|
| 31               | Reserved    |
| 21-20           | PMS CORE X IRAMO PMS CONSTRAINT CONRAIN_1 PMS 0 |
| 18-17           | PMS CORE X IRAMO PMS CONSTRAINT CONRAIN_1 PMS 1 |
| ...             | ...         |
| 3-2             | PMS CORE X IRAMO PMS CONSTRAINT CONRAIN_1 PMS 6 |

**Descriptions:**

- **PMS_CORE_X_IRAMO_PMS CONSTRAINT_SRAM_WORLD_1_PMS_0**
  - Configures the permission of CPU’s IBUS to instruction region0 of SRAM from the Non-secure World. (R/W)

- **PMS CORE X IRAMO PMS CONSTRAINT_SRAM_WORLD_1_PMS_1**
  - Configures the permission of CPU’s IBUS to instruction region1 of SRAM from the Non-secure World. (R/W)

- **PMS CORE X IRAMO PMS CONSTRAINT_SRAM_WORLD_1_PMS_2**
  - Configures the permission of CPU’s IBUS to instruction region2 of SRAM from the Non-secure World. (R/W)

- **PMS CORE X IRAMO PMS CONSTRAINT_SRAM_WORLD_1_PMS_3**
  - Configures the permission of CPU's IBUS to data region of SRAM from the Non-secure World. It’s advised to configure this field to O. (R/W)

**Footer:**
Continued on the next page...