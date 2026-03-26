

```markdown
Register 10.46. HP_SYS_CLKRST_DPA_CTRL0_REG (0x00B8)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 3   | HP_SYS_CLKRST_SEC_DPA_CFG_SEL  | Configures the source of the security level of CRYPTO_CLK against DPA attacks. <br> O: The security level is determined by EFUSE_SEC_DPA_LEVEL <br> 1: The security level is determined by HP_SYS_CLKRST_SEC_DPA_LEVEL (R/W) |
| 2   |                                |                                                                             |
| 1   | HP_SYS_CLKRST_SEC_DPA_LEVEL     | Configures the security level of CRYPTO_CLK against DPA attacks. <br> O: Low security level <br> 1: High security level (R/W) |

```markdown
Espressif Systems
717
ESP32-P4 TRM
PRELIMINARY
Submit Documentation Feedback
```