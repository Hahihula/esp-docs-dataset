**Title:**
3 Boot Configurations

**Table Title:**
Table 3-5. JTAG Signal Source Control

| JTAG Signal Source | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_STRAP_JTAG_SEL | GPIO3 |
|--------------------|---------------------|---------------------|------------------------|-------|
| USB Serial/JTAG Controller | O | 0 | 1 | Ignored |
|                             | 1 | O |     |       |
| JTAG pins^2                | O | 0 | 1 |    | Ignored |
|                             | 0 | 1 |     |      |        |
| JTAG is disabled           | 1 | 1 |     |      |        |

**Footnotes:**
1. Bold marks the default value and configuration.
2. JTAG pins refer to MTDI, MTCK, MTMS, and MTDO.

**Footer Information:**
Espressif Systems
ESP32-S3 Series Datasheet v2.1

Submit Documentation Feedback