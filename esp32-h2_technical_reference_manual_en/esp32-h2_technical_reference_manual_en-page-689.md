

```markdown
Chapter 26 External Memory Encryption and Decryption (XTS_AES) GoBack

The total number of pseudo-rounds that will be randomly inserted into each XTS-AES operation round is controlled by:

*   `pseudo_base`: configures the basic round number of pseudo-round function.
*   `pseudo_inc`: configures the random incremental round number of pseudo-round function.

The total number of pseudo-rounds will be randomly in the range

[pseudo_base, pseudo_base + (2^pseudo_inc - 1)]

Random number update frequency

`pseudo_rnd_cnt` configures the frequency of random key updates in the pseudo-round function. The higher the configured value, the higher the update frequency. This value is usually recommended to be set to maximum (7).

Configuration

The parameters mentioned above can be configured through eFuse bits or XTS_AES related registers, depending on the value of `EFUSE_XTS_DPA_PSEUDO_LEVEL`:

*   0: The user can configure using XTS_AES related registers.
*   1, 2, or 3: User configuration is not allowed.

See Table 26.6-1 for details.

Table 26.6-1. Configuration of XTS_AES Pseudo-round Anti-DPA

| EFUSE_XTS_DPA_PSEUDO_LEVEL | pseudo_mode         | pseudo_base             | pseudo_inc              | pseudo_rnd_cnt          |
|----------------------------|---------------------|-------------------------|-------------------------|--------------------------|
| 0                          | XTS_AES_PSEUDO_MODE | XTS_AES_PSEUDO_BASE     | XTS_AES_PSEUDO_INC      | XTS_AES_PSEUDO_RNG_CNT   |
| 1                          | 1                   | 4                       | 2                       | 7                        |
| 2                          | 2                   | 4                       | 2                       | 7                        |
| 3                          | 3                   | 4                       | 2                       | 7                        |
```