

```markdown
Register 40.38. CSI_HOST_INT_FORCE_ECC_CORRECTED_REG (0x02D8)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 15-0| CSI_HOST_FORCE_ERR_ECC_CORRECTED_VC[15:0]   | Configures whether to force set CSI_HOST_ST_ERR_ECC_CORRECTED_VC[n] to 1.    |
|     |                                             | 0: Do not force set                                                         |
|     |                                             | 1: Force set                                                                |
|     | (R/W)                                      |                                                                             |

Register 40.39. CSI_HOST_PHY_STOPSTATE_REG (0x004C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 16-17| CSI_HOST_PHY_STOPSTATECLK                  | Represents whether clock lane is in stop state.                             |
|     |                                             | 0: Not in stop state                                                        |
|     |                                             | 1: In stop state                                                             |
|     | (RO)                                       |                                                                             |
| 2-0 | CSI_HOST_PHY_STOPSTATEDATA_[1:0]           | Represents whether data lane n is in stop state.                            |
|     |                                             | 0: Not in stop state                                                        |
|     |                                             | 1: In stop state                                                             |
|     | (RO)                                       |                                                                             |

Espressif Systems    2099    ESP32-P4 TRM
Submit Documentation Feedback   PRELIMINARY
```