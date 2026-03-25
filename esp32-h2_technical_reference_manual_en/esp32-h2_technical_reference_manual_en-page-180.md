

```markdown
Chapter 5 eFuse Controller (EFUSE)
Register 5.17. EFUSE_RD_REPEAT_DATA4_REG (0x0040)

| 31 | 24 | 23 | 22 | 21 |
|----:|----:|----:|----:|----:|
|   OxO |   OxO |     |     | Reset |

EFUSE_RPT4_RESERVED4_0 Reserved. (RO)
EFUSE_RPT4_RESERVED4_1 Reserved. (RO)

EFUSE_HYS_EN_PAD1 Represents whether to enable the hysteresis function of pad 6-27.
0: Disabled
1: Enabled
(RO)

Register 5.18. EFUSE_RD_MAC_SYS_O_REG (0x0044)

| 31 |
|----|
|   Ox000000 | Reset |

EFUSE_MAC_0 Represents the low 32 bits of MAC address. (RO)

Register 5.19. EFUSE_RD_MAC_SYS_1_REG (0x0048)

| 31 |    16 | 15 |
|----:|-------:|----:|
|   OxO |       | Reset |

EFUSE_MAC_1 Represents the high 16 bits of MAC address. (RO)
EFUSE_MAC_EXT Represents the extended bits of MAC address. (RO)

Espressif Systems
180
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```