

```markdown
Register 29.6. XTS_AES_PSEUDO_ROUND_CONF_REG (0x038C)

| Bit | Name                        | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 11  | XTS_AES_PSEUDO_INC          | Configures the incremental round number of pseudo-round Anti-DPA function. (R/W) |
| 10  | XTS_AES_PSEUDO_BASE         | Configures the basic round number of pseudo-round Anti-DPA function. (R/W)     |
| 9   | XTS_AES_PSEUDO_RNG_CNT      | Configures the update frequency of the pseudo-key in the pseudo-round Anti-DPA function. (R/W) |
| 7   | XTS_AES_PSEUDO_MODE         | Set the calculation steps of XTS-AES to enable pseudo-round Anti-DPA function.<br>0: not enable the pseudo-round Anti-DPA function during calculation<br>1: enable the pseudo-round Anti-DPA function when calculating Tweak value<br>2: enable the pseudo-round Anti-DPA function when calculating Tweak value and some rounds of calculating Data units<br>3: enable the pseudo-round Anti-DPA function when calculating Tweak value and all rounds of calculating Data units (R/W) |
| 6-4 | Reserved                    |                                                                             |
| 3   | XTS_AES_PSEUDO_RNG_CNT      |                                                                             |
| 2   | XTS_AES_PSEUDO_BASE         |                                                                             |
| 1   | XTS_AES_PSEUDO_INC          |                                                                             |
| 0   | Reset                      |                                                                             |

Register 29.7. XTS_AES_TRIGGER_REG (0x034C)

| Bit | Name                        | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 1   | XTS_AES_TRIGGER             | Set this bit to trigger the process of manual encryption calculation.<br>0: Disable manual encryption<br>1: Enable manual encryption<br>This action should only be asserted when manual encryption status is 0. After this action, manual encryption status becomes 1. After calculation is done, manual encryption status becomes 2. (WT) |
| 0   | Reset                      |                                                                             |
```