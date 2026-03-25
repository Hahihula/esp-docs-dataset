

```markdown
Register 30.3. HINF_CFG_DATA7_REG (0x001C)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 30        | HINF_SDIO_WAKEUP_CLR           | Configures whether to clear wake up signal after the chip is waken up by the SDIO slave. <br> O: No effect <br> 1: Clear (WT) |
| 29        |                                |                                                                             |
| 20..18    | HINF_ESDIO_DATA1_INT_EN        | Configures whether to enable SDIO interrupt on data1 line. <br> O: Disable <br> 1: Enable (R/W) |
| 17..16    | HINF_SDIO_RST                  | Configures whether to reset the SDIO slave module. <br> O: No effect <br> 1: Reset (R/W) |
| 15        | HINF_CHIP_STATE                | Configures SDIO CIS address 312, 315, 568, and 571. Please refer to SDIO Specification for details. (R/W) |
| 8..0      | HINF_PIN_STATE                 | Configures SDIO CIS address 318 and 574. Please refer to SDIO Specification for details. (R/W) |

Register 30.4. HINF_CIS_CONF_Wn_REG(n: 0-7) (0x0020+0x4*n)
```