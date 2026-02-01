**Title:**
3 Boot Configurations

**Table Title:**
Table 3-6. JTAG Signal Source Control

| JTGA Signal Source | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_STRAP_JTAG_SEL_ENABLE | GPIO25 |
|--------------------|---------------------|--------------------|-------------------------------|--------|
| USB Serial/JTAG Controller | - | 0 | 1 | Ignored |
| JTAG pins^2       | O                   |                    |                               |        |
| USB Serial/JTAG Controller |   |    |     |         |
| JTAG pins^2       | O                   | 1                  | Ignored                       |        |
| USB Serial/JTAG Controller | - | 0 | Ignored |        |
| JTAG is disabled  | 1                   |                    |                               | Ignored |

**Footnotes:**
1. Bold marks the default value and configuration.
2. JTAG pins refer to MTDI, MTCK, MTMS, and MTDO.

**Footer Information:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2

Submit Documentation Feedback