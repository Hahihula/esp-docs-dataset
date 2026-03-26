

```markdown
| Bit Field | Description |
|-----------|-------------|
| EFUSE_DIS_SWD_ERR | This bit being 1 represents a programming error of DIS_SWD. (RO) |
| EFUSE_DIS_WDT_ERR | This bit being 1 represents a programming error of DIS_WDT. (RO) |
| EFUSE_DCDC_VSET_EN_ERR | This bit being 1 represents a programming error of DCDC_VSET_EN. (RO) |
| EFUSE_HP_PWR_SRC_SEL_ERR | This bit being 1 represents a programming error of HP_PWR_SRC_SEL. (RO) |
| EFUSE_USB_OTG11_DREFL_ERR | Any bit of this field being 1 represents a programming error of USB_OTG11_DREFL. (RO) |
| EFUSE_USB_DEVICE_DREFL_ERR | Any bit of this field being 1 represents a programming error of USB_DEVICE_DREFL. (RO) |
| EFUSE_OPXA_TIEH_SEL_3_ERR | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_3. (RO) |
| EFUSE_OPXA_TIEH_SEL_2_ERR | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_2. (RO) |
| EFUSE_OPXA_TIEH_SEL_1_ERR | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_1. (RO) |
| EFUSE_OPXA_TIEH_SEL_0_ERR | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_0. (RO) |
```

Register 8.28. EFUSE_RD_REPEAT_ERR4_REG (0x018C)

```markdown
| Bit Position | Field Name                     | Description                                                                 |
|--------------|---------------------------------|-----------------------------------------------------------------------------|
| 31           | (reserved)                     |                                                                             |
| 30           | EFUSE_DIS_SWD_ERR              | This bit being 1 represents a programming error of DIS_SWD. (RO)             |
| 29           | EFUSE_DIS_WDT_ERR              | This bit being 1 represents a programming error of DIS_WDT. (RO)             |
| 28           | EFUSE_DCDC_VSET_EN_ERR         | This bit being 1 represents a programming error of DCDC_VSET_EN. (RO)        |
| 27           | EFUSE_HP_PWR_SRC_SEL_ERR       | This bit being 1 represents a programming error of HP_PWR_SRC_SEL. (RO)     |
| 26           | EFUSE_USB_OTG11_DREFL_ERR      | Any bit of this field being 1 represents a programming error of USB_OTG11_DREFL. (RO) |
| 25           | EFUSE_USB_DEVICE_DREFL_ERR     | Any bit of this field being 1 represents a programming error of USB_DEVICE_DREFL. (RO) |
| 24           | EFUSE_OPXA_TIEH_SEL_3_ERR      | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_3. (RO) |
| 23           | EFUSE_OPXA_TIEH_SEL_2_ERR      | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_2. (RO) |
| 22           | EFUSE_OPXA_TIEH_SEL_1_ERR      | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_1. (RO) |
| 21           | EFUSE_OPXA_TIEH_SEL_0_ERR      | Any bit of this field being 1 represents a programming error of OPXA_TIEH_SEL_0. (RO) |
| 20-16        | (reserved)                     |                                                                             |
| 15           | O                              |                                                                             |
| 14           | OxO                             |                                                                             |
| 13           | OxO                             |                                                                             |
| 12           | OxO                             |                                                                             |
| 11           | OxO                             |                                                                             |
| 10-8         | (reserved)                     |                                                                             |
| 7            | O                              |                                                                             |
| 6            | OxO                             |                                                                             |
| 5            | OxO                             |                                                                             |
| 4            | OxO                             |                                                                             |
| 3            | OxO                             |                                                                             |
| 2            | OxO                             |                                                                             |
| 1            | OxO                             |                                                                             |
| 0            | Reset                           |                                                                             |
```