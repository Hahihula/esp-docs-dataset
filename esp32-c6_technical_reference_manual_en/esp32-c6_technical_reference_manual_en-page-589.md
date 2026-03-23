

```markdown
Register 16.44. LP_APMO_REGIONn_ATTR_REG (n: 0-3) (0x000C+0xC*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | LP_APMO_REGIONn_RO_X           | Configures region execute authority in REE_MODE0 (R/W)                      |
| 29  | LP_APMO_REGIONn_RO_W           | Configures region write authority in REE_MODE0 (R/W)                        |
| 28  | LP_APMO_REGIONn_RO_R           | Configures region read authority in REE_MODE0 (R/W)                         |
| 27  | LP_APMO_REGIONn_R1_X           | Configures region execute authority in REE_MODE1 (R/W)                      |
| 26  | LP_APMO_REGIONn_R1_W           | Configures region write authority in REE_MODE1 (R/W)                        |
| 25  | LP_APMO_REGIONn_R1_R           | Configures region read authority in REE_MODE1 (R/W)                         |
| 24  | LP_APMO_REGIONn_R2_X           | Configures region execute authority in REE_MODE2 (R/W)                      |
| 23  | LP_APMO_REGIONn_R2_W           | Configures region write authority in REE_MODE2 (R/W)                        |
| 22  | LP_APMO_REGIONn_R2_R           | Configures region read authority in REE_MODE2 (R/W)                         |

Register 16.45. LP_APMO_FUNC_CTRL_REG (0x00C4)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | LP_APMO_MO_FUNC_EN             | Configures to enable APM MO function. (R/W)                                 |

```
```plaintext
GoBack

Espressif Systems    589    ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```