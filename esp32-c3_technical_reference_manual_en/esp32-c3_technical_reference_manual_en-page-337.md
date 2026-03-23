

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Configuration Registers                    |                                                                                                  |           |        |
| SYSCON_EXT_MEM_PMS_LOCK_REG               | External Memory Permission Lock Register                                                        | 0x0020    | R/W    |
| SYSCON_FLASH_ACEn_ATTR_REG (n: 0 - 3)     | Flash Area Permission Config Register                                                          | 0x0028 + 4 * n | R/W    |
| SYSCON_SRAM_ACEn_ADDR_S (n: 0 - 3)        | Flash Area Starting Address Config Register                                                    | 0x0038 + 4 * n | R/W    |
| SYSCON_FLASH_ACEn_SIZE_REG (n: 0 - 3)     | Flash Area Length Config Register                                                              | 0x0048 + 4 * n | R/W    |
| SYSCON_SPI_MEM_PMS_CTRL_REG               | External Memory Unauthorized Access Interrupt Register                                          | 0x0088    | varies |
| SYSCON_SPI_MEM_REJECT_ADDR_REG            | External Memory Unauthorized Access Address Register                                           | 0x008C    | RO     |

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Permission Configure register              |                                                                                                  |           |        |
| EXTMEM_IBUS_PMS_TBL_LOCK_REG              | Cache IBUS Regions Lock                                                                         | 0x00D8    | R/W    |
| EXTMEM_IBUS_PMS_TBL_BOUNDARYn_REG (n: 0 - 2)| Cache IBUS Region(n+1) Starting Address Config Register                                        | 0x00DC + 4 * n | R/W    |
| EXTMEM_IBUS_PMS_TBL_ATTR_REG               | Cache IBUS Region Permission Register                                                           | 0x00E8    | R/W    |
| EXTMEM_DBUS_PMS_TBL_LOCK_REG               | Cache DBUS Regions Lock                                                                         | 0x00EC    | R/W    |
| EXTMEM_DBUS_PMS_TBL_BOUNDARYn_REG (n: 0 - 2)| Cache DBUS Region(n+1) Starting Address Config Register                                        | 0x00FO + 4 * n | R/W    |
| EXTMEM_DBUS_PMS_TBL_ATTR_REG               | Cache DBUS Region Permission Register                                                           | 0x00FC    | R/W    |
```