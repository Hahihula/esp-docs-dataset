

```markdown
| Purpose               | Mode    | Value | Description                                                                 |
|-----------------------|---------|-------|-----------------------------------------------------------------------------|
| JTAG Re-enable        | Downstream | 6     | EFUSE_KEY_PURPOSE_HMAC_DOWN_JTAG                                            |
| DS KDF                | Downstream | 7     | EFUSE_KEY_PURPOSE_HMAC_DOWN_DIGITAL_SIGNATURE                              |
| HMAC Calculation      | Upstream   | 8     | EFUSE_KEY_PURPOSE_HMAC_UP                                                    |
| Both JTAG Re-enable and DS KDF | Downstream | 5     | EFUSE_KEY_PURPOSE_HMAC_DOWN_ALL                                             |

## Configure HMAC Purposes

The correct purpose has to be written to register `HMAC_SET_PARA_PURPOSE_REG` (see Section 21.2.5). If there is no valid value in eFuse purpose section, HMAC will terminate calculation.
```