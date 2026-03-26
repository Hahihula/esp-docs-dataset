

```markdown
- reg_anti_dpa_level = XTS_AES_CRYPTO_SECURITY_LEVEL
- efuse_anti_dpa_level = 3

* Configure the security level of Anti-DPA for the XTS-AES module:

Anti_DPA_level = select_reg ? (reg_anti_dpa_level) : (efuse_dpa_en * efuse_anti_dpa_level)

When `Anti_DPA_level` equals 0, Anti-DPA is disabled. The higher the value of `Anti_DPA_level` is, the stronger the Anti-DPA ability is.

* Configure whether to enable Anti-DPA when the XTS-AES algorithm is calculating D:

Anti_DPA_enabled_in_calc_D = select_reg ? reg_d_dpa_en : efuse_dpa_en

If `Anti_DPA_level` is not 0, when `Anti_DPA_enabled_in_calc_D` equals to 1, Anti-DPA is enabled when XTS-AES algorithm is calculating D.

If `Anti_DPA_level` is not 0, Anti-DPA is always enabled when the XTS-AES algorithm is calculating T.
```

**Note:**

* Even if `efuse_dpa_en` is set to 1, you can still disable anti-DPA by configuring `select_reg = 1` and `reg_anti_dpa_level = 0`.
* Configuring whether or not to enable Anti-DPA will have an impact on the external storage access bandwidth:
    - When Anti-DPA is enabled during the calculation of D, the read and write bandwidth will be reduced by more than 50% when the Anti-DPA level >= 4.
    - When Anti-DPA is disabled during the calculation of D, the read and write bandwidth will be reduced by more than 50% when the Anti-DPA level >= 6.
```