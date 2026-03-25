

```markdown
Register 26.6. XTS_AES_PSEUDO_ROUND_CONF_REG (0x038C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 11  | XTS_AES_PSEUDO_INC             | Configures the incremental round number of pseudo-round Anti-DPA function. (R/W) |
| 10  | XTS_AES_PSEUDO_BASE            | Configures the basic round number of pseudo-round Anti-DPA function. (R/W)    |
| 9   | XTS_AES_PSEUDO_RNG_CNT         | Configures the update frequency of the pseudo-key in the pseudo-round Anti-DPA function. (R/W) |
| 7   | XTS_AES_MODE_PSEUDO            | Set the calculation steps of XTS-AES to enable pseudo-round Anti-DPA function.<br>0: not enable the pseudo-round Anti-DPA function during calculation<br>1: enable the pseudo-round Anti-DPA function when calculating Tweak value<br>2: enable the pseudo-round Anti-DPA function when calculating Tweak value and some rounds of calculating Data units<br>3: enable the pseudo-round Anti-DPA function when calculating Tweak value and all rounds of calculating Data units (R/W) |
| 6   | XTS_AES_PSEUDO_RNG_CNT         | Configures the update frequency of the pseudo-key in the pseudo-round Anti-DPA function. (R/W) |
| 5   | XTS_AES_PSEUDO_BASE            | Configures the basic round number of pseudo-round Anti-DPA function. (R/W)    |
| 4   | XTS_AES_PSEUDO_INC             | Configures the incremental round number of pseudo-round Anti-DPA function. (R/W) |

Register 26.7. XTS_AES_TRIGGER_REG (0x034C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 1   | XTS_AES_TRIGGER               | Configures whether or not to enable manual encryption.<br>0: Disable manual encryption<br>1: Enable manual encryption (WO) |
```