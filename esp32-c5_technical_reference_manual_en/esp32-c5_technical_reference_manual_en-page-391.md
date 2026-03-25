

```markdown
PLL_F480M_CLK

PLL_F480M_CLK is a 480 MHz clock. PLL_F240M_CLK, PLL_F160M_CLK, PLL_F80M_CLK, PLL_F48M_CLK and PLL_F40M_CLK are divided from PLL_F480M_CLK.

CRYPTO_CLK

As shown in Figure 9.2-3, CRYPTO_CLK can be derived from XTAL_CLK, PLL_F480M_CLK, or RC_FAST_CLK, and its frequency is up to 160 MHz.

To protect encryption and decryption peripherals from DPA (Differential Power Analysis) attacks, a random divider strategy is implemented for the functional clock of these peripherals. Four security levels are available, depending on the range of random divider. Users can select the security level by configuring HP_SYSTEM_SEC_DPA_CONF_REG. If HP_SYSTEM_SEC_DPA_CFG_SEL is set to 1, the security level is determined by the configuration of EFUSE_SEC_DPA_LEVEL, otherwise, by the value of HP_SYSTEM_SEC_DPA_LEVEL.

LED_PWM Clock

LEDC module uses PLL_F80M_CLK, RC_FAST_CLK or XTAL_CLK as its clock source. When the system is in low-power mode (APB_CLK is disabled), most peripherals are halted, but LEDC can still work via RC_FAST_CLK.

Slow Clock for Timer Group O

Using XTAL_CLK as a reference, TIMGO can calculate the frequency of slow clock sources provided by ESP32-C5. The slow clock source can be selected by configuring PCR_32K_SEL:

0: Select XTAL32K_CLK clock
1: Select OSC_SLOW_CLK clock
2: Select RC_SLOW_CLK clock
3: Select RC_FAST_CLK clock

Low-Power System Clock Registers

See 9.4.2 LP System Clock Register Summary for the clock registers of low-power system peripherals.

9.2.4.4 PMU Control of High-Performance System Clock Gating

In various operating modes of ESP32-C5, the following register fields can be pre-configured to enable the Power Management Unit (PMU) to control the clock gating of high-performance system peripherals:

*   `PMU_HP_x_DIG_ICG_APB_EN` (x = ACTIVE/MODEM/SLEEP): Controls the clock gating for reading and writing registers of high-performance system peripherals.
*   `PMU_HP_x_DIG_ICG_FUNC_EN` (x = ACTIVE/MODEM/SLEEP): Controls the functional clock gating of high-performance system peripherals.

For the specific configuration process, please refer to the Chapter 13 Low-Power Management.

Tables 9.2-7 and 9.2-8 list the correspondence between PMU pre-configured register bits and high-performance system clock gating.
```