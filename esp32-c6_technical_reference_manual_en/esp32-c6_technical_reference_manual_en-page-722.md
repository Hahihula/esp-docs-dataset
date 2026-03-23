

```markdown
When `Anti_DPA_level` equals to 0, Anti-DPA is disabled. The higher the value of `Anti_DPA_level` is, the stronger the Anti-DPA ability is.

* Configure whether or not to enable Anti-DPA when the XTS-AES algorithm is calculating D:

    ``` Anti_DPA_enabled_in_calc_D = select_reg ? reg_d_dpa_en : efuse_dpa_en ```

If `Anti_DPA_level` is not 0, when `Anti_DPA_enabled_in_calc_D` equals to 1, Anti-DPA is enabled when XTS-AES algorithm is calculating D.

If `Anti_DPA_level` is not 0, Anti-DPA is always enabled when the XTS-AES algorithm is calculating T.
```

```markdown
Note:
Configuring whether or not to enable Anti-DPA will have an impact on the external storage access bandwidth:

* When Anti-DPA is enabled during the calculation of D, the read and write bandwidth will be significantly impacted when the Anti-Attack level >= 4.
* When Anti-DPA is disabled during the calculation of D, the read and write bandwidth will be significantly impacted when the Anti-Attack level >= 6.
```