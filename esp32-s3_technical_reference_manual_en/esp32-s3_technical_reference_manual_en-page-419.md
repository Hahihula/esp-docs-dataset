**Chapter 5: eFuse Controller**

When `EFUSE_BLK_NUM` is set to 0, BLOCK0 will be programmed. Register `EFUSE_PGM_DATAO_REG` stores `EFUSE_WR_DIS`. Registers `EFUSE_PGM_DATA1_REG`, `EFUSE_PGM_DATA2_REG`, and so on in the programming registers.

- **EFUSE_PGM_DATA1_REG[27:31]**
- **EFUSE_PGM_DATA1_REG[21:24]**
- **EFUSE_PGM_DATA2_REG[7:15]**
- **EFUSE_PGM_DATA2_REG[0:3]**
- **EFUSE_PGM_DATA3_REG[26:27]**
- **EFUSE_PGM_DATA4_REG[30]**

Data in registers `EFUSE_PGM_DATA6_REG`, `EFUSE_PGM_DATA7_REG` and so on are ignored when programming BLOCK0.

**Programming BLOCK1**

When `EFUSE_BLK_NUM` is set to 1, registers `EFUSE_PGM_DATAO_REG`, `EFUSE_PGM_DATA5_REG` store the corresponding parameters to be programmed. Registers `EFUSE_PGM_CHECK_VALUEO_REG` and so on are ignored when programming BLOCK1.

- **EFUSE_PGM_CHECK_VALUE2_REG** stores RS check codes.
- Data in registers `EFUSE_PGM_DATA6_REG`, `EFUSE_PGM_DATA7_REG` is ignored, the RS check codes will be calculated with these bits all treated as 0.

**Programming BLOCK2 ~ 10**

When `EFUSE_BLK_NUM` is set to 2~10, registers `EFUSE_PGM_DATAO_REG`, and so on store parameters for programming this block. Registers in `EFUSE_PGM_CHECK_VALUEO_REG` are RS check codes corresponding to the data.

**Programming process**

The steps of parameter setting include:

1. Write the block number to determine which block is programmed.
2. Set parameters as required, including checksum values and so on:
   - **EFUSE_PGM_DATA0_REG**
   - **EFUSE_PGM_CHECK_VALUEO_REG**
3. Configure `EFUSE_OP_CODE` field in register `EFUSE_CONF_REG`.
4. Configure the field of `EFUSE_CMD` to 1.
5. Poll until a PGM_DONE interrupt occurs, or wait for it if necessary.

**Additional notes:**

- To avoid programming content leakage:
   - Clear parameters from specific registers (`EFUSE_PGM_DATAO_REG`, etc.) before operation completion in Section [5.3.3](#).

**Trigger an eFuse read operation**: Refer to section 5.3.3 for updating `eFuse` with new values.

---

*Espressif Systems*

*419 ESP32-S3 TRM (Version 1.7)*

[Submit Documentation Feedback]