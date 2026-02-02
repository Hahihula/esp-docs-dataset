**Chapter Title:**
Chapter 7 Reset and Clock

**Body Text:**
carry jitter and, therefore, they do not support a high-precision clock frequency setting.

Providing an integrated precision clock source can minimize system cost. To this end, ESP32 integrates an audio PLL.
The Audio PLL formula is as follows:
\[ f_{\text{out}} = \frac{f_{\text{xtal}}(s\text{dm}2 + \frac{s\text{dm1}}{2^{\text{s\text{dm1}}}} + \frac{s\text{dm0}}{2^{\text{s\text{dm0}}}} + 4)}{2(\text{odiv} + 2)} \]

**Subsection Title:**
The parameters of this formula are defined below:

- \( f_{\text{xtal}} \): the frequency of the crystal oscillator, usually 40 MHz;
- s\text{dm0}: the value is 0 ~ 255;
- s\text{dm1}: the value is 0 ~ 255;
- s\text{dm2}: the value is 0 ~ 63;
- odiv: the value is 0 ~ 31;

The operating frequency range of the numerator is 350 MHz ~ 500 MHz

\[ 350MHz < f_{\text{xtal}}(s\text{dm}2 + \frac{s\text{dm1}}{2^{\text{s\text{dm1}}}} + \frac{s\text{dm0}}{2^{\text{s\text{dm0}}}} + 4) < 500MHz \]

**Note:**
Please note that s\text{dm}1 and s\text{dm}0 are not available on revision 0 of ESP32. Please consult the silicon revision in ESP32 Series SoC Errata for further details.

Audio PLL can be manually enabled or disabled via registers RTC_CNTL_PLLA FORCE PU and RTC_CNTL_PLLA FORCE PD, respectively. Disabling it takes priority over enabling it. When RTC_CNTL_PLLA FORCE PU and RTC_CNTL_PLLA FORCE PD are 0, PLL will follow the state of the system; i.e., when the system enters sleep mode, PLL will be disabled automatically; when the system wakes up, PLL will be enabled automatically.

**Subsection Title:**
7.3 Register Summary

The addresses in this section are relative to the SYSCON base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory:

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Configuration register | Configures system clock frequency | 0x0000 R/W | |
| SYSCON_SYSTICK_CONF_REG | Configures the divider value of REF_TICK | 0x0004 R/W | |
| SYSCON_PLL_TICK_CONF_REG | Configures the divider value of REF_TICK | 0x0008 R/W | |
| SYSCON_CK8M_TICK_CONF_REG | Configures the divider value of REF_TICK | 0x000C R/W | |
| SYSCON_APLL_TICK_CONF_REG | Configures the divider value of REF_TICK | 0x003C R/W | |

**Subsection Title:**
Chip revision register

SYSCON_DATE_REG Chip revision register
OXO07C R/W