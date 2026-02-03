**Title: Chapter 5 eFuse Controller**

**Subtitle: Register 5.103. EFUSE_CLK_REG (0x01C8)**

**Diagram Description:** Binary register diagram with labels and values.

- **EFUSE_CLK_EN**: (reserved)
- **EFUSE_MEM_FORC_PD**: (reserved)

**Binary Values in Diagram:**
```
0 0 0 0 0 0 0 0 0 0 0 0 0 1 0
```

**Text Descriptions and Definitions for Binary Fields:**

- **EFUSE_EFUSE_MEM_FORC_PD**: Configures whether or not to force eFuse SRAM into power-saving mode. 
  - Values:
    - `1`: Force.
    - `0`: No effect.

- **EFUSE_MEM_CLK FORCE_ON**: Configures whether or not to force on activate clock signal of eFuse
  - Values:
    - `SRAM`: `1`: Force, `0`: No effect. (R/W)

- **EFUSE_EFUSE_MEM_FORC_PU**: Configures whether or not to force eFuse SRAM into working mode.
  - Values:
    - `1`: Force, `0`: No effect.

- **EFUSE_CLK_EN**: Configures whether or not to enable clock signal of eFuse registers. 
  - Values:
    - `1`: Enable
    - `0`: No effect

**Subtitle: Register 5.104. EFUSE_CONF_REG (0x01CC)**

**Diagram Description:** Binary register diagram with labels and values.

- **EFUSE_OP_CODE**: (reserved)
- **EFUSE_MEM_FORC_PD**: (reserved)

**Binary Values in Diagram:**
```
0 0 0 0 0 0 0 0 0 0 0 0 0 1 0
```

**Text Descriptions and Definitions for Binary Fields:**

- **EFUSE_OP_CODE**: Configures whether to operate programming command or read command.
  - Values:
    - `0x5A5A`: Operate programming command. (R/W)
    - `0x5AA5`: Operate read command.

**Footer Information:** 
- Page number: "466"
- Company name and document version information at the bottom of each page.
  - Espressif Systems
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback