

```markdown
Note:
To protect the encryption and decryption peripherals from DPA (Differential Power Analysis) attacks, a random divider strategy is implemented for its function clock. Four security levels are available, depending on the range of the random divider. Users can select the security level by configuring HP_SYS_CLKRST_SEC_DPA_CFG_SEL.
If HP_SYS_CLKRST_SEC_DPA_CFG_SEL is set to 1, the security level is determined by the configuration of HP_SYS_CLKRST_SEC_DPA_LEVEL. Otherwise, the security level is determined by the value of EFUSE_SEC_DPA_LEVEL.

## 10.3 Programming Procedures

### 10.3.1 HP System Clock Configuration

*   Configure the clock divisor for CPU_CLK: `HP_SYS_CLKRST_CPU_CLK_DIV_NUM` for the integral part, `HP_SYS_CLKRST_CPU_CLK_DIV_NUMERATOR` for the numerator of the fractional part, and `HP_SYS_CLKRST_CPU_CLK_DIV_DENOMINATOR` for the denominator of the fractional part.
    Write 1 to `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` to apply the frequency divisor configurations for CPU_CLK.

*   Configure the clock divisor for MEM_CLK: `HP_SYS_CLKRST_MEM_CLK_DIV_NUM` for the integral part, `HP_SYS_CLKRST_MEM_CLK_DIV_NUMERATOR` for the numerator of the fractional part, and `HP_SYS_CLKRST_MEM_CLK_DIV_DENOMINATOR` for the denominator of the fractional part.
    Write 1 to `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` to apply the frequency divisor configurations for MEM_CLK.

*   Configure the clock divisor for SYS_CLK: `HP_SYS_CLKRST_SYS_CLK_DIV_NUM` for the integral part, `HP_SYS_CLKRST_SYS_CLK_DIV_NUMERATOR` for the numerator of the fractional part, and `HP_SYS_CLKRST_SYS_CLK_DIV_DENOMINATOR` for the denominator of the fractional part.
    Write 1 to `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` to apply the frequency divisor configurations for SYS_CLK.

*   Configure the clock divisor for APB_CLK: `HP_SYS_CLKRST_APB_CLK_DIV_NUM` for the integral part, `HP_SYS_CLKRST_APB_CLK_DIV_NUMERATOR` for the numerator of the fractional part, and `HP_SYS_CLKRST_APB_CLK_DIV_DENOMINATOR` for the denominator of the fractional part.
    Write 1 to `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` to apply the frequency divisor configurations for APB_CLK.

*   Configure the clock source for ROOT_CLK via `LP_CLKRST_HP_ROOT_CLK_SRC_SEL`.

**Notice:**
1.  It is recommended to first configure the frequency divisors for the SoC clocks and apply the configurations, and then configure the clock source for ROOT_CLK.
2.  Before changing the clock source for ROOT_CLK, software needs to ensure that the configured clock divisors do not result in clock frequencies exceeding the allowed maximum frequencies.
3.  Writing 1 to `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` will apply the frequency divisor configurations for CPU_CLK, MEM_CLK, SYS_CLK, and APB_CLK at one go, but it is not recommended to do so. It would be better to apply the configuration for each clock individually.
4.  When switching from a high divisor to a low divisor, the recommended configuration order is APB_CLK
```