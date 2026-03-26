

```markdown
| Chip Pins | SAR ADC Channel | SAR ADC Selection |
|-----------|-----------------|-------------------|
| GPIO51    | 2               |                   |
| GPIO52    | 3               |                   |
| GPIO53    | 4               |                   |
| GPIO54    | 5               |                   |

## 62.5.3 SAR ADC Clock

The clock for the HP ADCx Controller has three possible sources, selected by `HP_SYS_CLKRST_ADC_CLK_SRC_SEL`:

*   XTAL_CLK
*   RC_FAST_CLK
*   PLL_F80M_CLK

The following clocks can be divided from the HP ADCx Controller's clock:

*   **HPADC_SARCLK**: It is the operating clock of HP ADCx and HP Readerx.
*   **HPADC_CLK**: It is the operating clock of HP ADC FSMx.

The frequency of HPADC_SARCLK can affect the sampling accuracy. If the HPADC_SARCLK frequency is higher than 5 MHz, the sampling accuracy will decrease. HPADC_SARCLK is divided from HPADC_CLK via a dedicated divider. The division is set in `ADC_SAR_CLK_DIV`.

It takes 25 HPADC_SARCLK clock cycles to complete one sampling, so the maximum sampling rate is limited by the frequency of HPADC_SARCLK.

The LP ADCx Controller is clocked from LP_DYN_FAST_CLK.

The following clocks can be divided from the LP ADCx Controller's clock:

*   **LPADC_SARCLK**: It is the operating clock of LP ADCx and LP Readerx. The division set in `LPADC_SAR1_CLK_DIV` and `LPADC_SAR2_CLK_DIV` should be at least 2. The frequency of LPADC_SARCLK should not exceed 5 MHz.
*   **LPADC_CLK**: It is the operating clock of LP ADC FSMx.

For more information about clocks, please refer to Chapter 10 Reset and Clock.

## 62.5.4 SAR ADC Conversion and Attenuation

The SAR ADCs can measure analog voltages from 0 mV to $V_{ref}$. $V_{ref}$ is the SAR ADCs' internal reference voltage. The conversion result (`data`) is a 12-bit digital value, which is the raw data. To calculate the voltage $V_{data}$ based on the raw data, the following formula can be used:

$$
V_{data} = \frac{V_{ref}}{4095} \times data
$$`

$k$ is the coefficient corresponding to the configured attenuation.

To convert voltages larger than $V_{ref}$, apply attenuation to the input signals. The supported attenuation levels are:
```