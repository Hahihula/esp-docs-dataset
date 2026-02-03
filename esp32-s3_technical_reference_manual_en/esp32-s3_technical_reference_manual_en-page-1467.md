**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Diagram Description (Figure):**
- **Figure Caption:** Figure 39.3-2. SAR ADC Architecture.
- The diagram shows the architecture of a SAR ADC module with various components connected to each other, including DIG_ADC1, DIG_ADC2, RTC, and clock management elements.

**Body Text:**

As shown in Figure 39.3-2, the SAR ADC module consists of the following components:

- **SAR ADC1:** measures voltages from up to 10 channels.
- **SAR ADC2:** measures the voltage from 10 channels.
- Clock management: selects clock sources and their dividers:
  - Clock source for DIG_ADC1 controller: APB_CLK or PLL_D2_CLK
  - Divided clocks of DIG_ADC1 controller:

    - DIGADC_SARCLK: operating clock for SAR ADC1, SAR ADC2, and Digital Reader1. Note that the divider (DIG_SAR_DIV) must be no less than 2, and the frequency of DIGADC_SARCLK must not exceed 5 MHz.
      See APB_SARADC_SAR_CLK_DIV.

    - DIGADC_CLK: operating clock for DIG_ADC FSM1.

- Clock source of RTC ADC1/2 controllers:
  - RTC_FAST_CLK

- Divided clock of RTC ADC1/2 controllers:

  - RTCAADC_SARCLK: operating clock for SAR ADC1, SAR ADC2, RTC Reader1, and RTC Reader2. Note that the divider (RTC_SAR_DIV) must be no less than 2, and the frequency of RTCAADC_SARCLK must not exceed 5 MHz.

- Arbiter (ADC2_ARBIT): this arbiter determines which controller is selected as the RTC ADC2 controller or PWDET controller. The arbiter also selects working clock for SAR ADC2 according to the authorized controller.

**Footer:**
Espressif Systems
1467 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback