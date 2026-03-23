

```markdown
PLL_CLK

PLL_F480M_CLK is the source clock of PLL which is 480 MHz. PLL_D2_CLK (240 MHz), PLL_F160M_CLK, PLL_F80M_CLK, and PLL_F48M_CLK are divided from PLL_F480M_CLK.

CRYPTO_CLK

As shown in Figure 8.2-1, CRYPTO_CLK shares the same clock sources with CPU_CLK, and its frequency is up to 160 MHz.

To protect encryption and decryption peripherals from DPA (Differential Power Analysis) attacks, a random divider strategy is implemented for the function clock of encryption and decryption peripherals. Four security levels are available, depending on the range of random divider. Users can select the security level by configuring HP_SYSTEM_SEC_DPA_CONF_REG. If HP_SYSTEM_SEC_DPA_CFG_SEL is set to 1, the security level is determined by configuration of EFUSE_SEC_DPA_LEVEL, otherwise, by the value of HP_SYSTEM_SEC_DPA_LEVEL.

LED_PWM

LEDC module uses PLL_F80M_CLK, RC_FAST_CLK and XTAL_CLK as clock source when APB_CLK is disabled. In other words, when the system is in low-power mode, most peripherals will be halted (APB_CLK is turned off), but LEDC can work normally via RC_FAST_CLK.

8.2.4.4 Wi-Fi and Bluetooth LE Clock

Wi-Fi and Bluetooth LE can work only when CPU_CLK uses PLL_CLK as its clock source. Suspending PLL_CLK requires that Wi-Fi and Bluetooth LE have entered low-power mode first.

8.2.5 HP System Clock Gating Controlled by PMU

In various operating modes of the ESP32-C6 chip, the following register fields can be pre-configured to enable the PMU to control the clock gating of HP system peripherals:

*   `PMU_HP_x_DIG_ICG_APB_EN` (x = ACTIVE/MODEM/SLEEP): Controls the clock gating of the register read/write operations of HP system peripherals.
*   `PMU_HP_x_DIG_ICG_FUNC_EN` (x = ACTIVE/MODEM/SLEEP): Controls the clock gating of the operating clock of HP system peripherals.

For detailed configuration procedures, please refer to 12 Low-Power Management.

Tables 8.2-6 and 8.2-7 list the correspondence between pre-configured PMU register bits and HP system clock gating.
```