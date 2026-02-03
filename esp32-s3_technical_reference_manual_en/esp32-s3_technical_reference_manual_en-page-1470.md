**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Section Titles with Subsections:**

1. **39.3.7 DIG ADC Controller**
   - The clock of the DIG ADC1 controller is quite fast, thus the sample rate is high.
     For more information, see Section ADC Characteristics in ESP32-S3 Series Datasheet.

   - Features:
     - up to 12-bit sampling resolution
     - timer-triggered multi-channel scanning

   - Configuration Instructions for DIG ADC Timer:
     - Configure APB_SARADC TIMER_TARGET: Set the trigger target for DIG ADC timer. When the timer counting reaches two times of the pre-configured cycle number, a sampling operation is triggered.
       For more details on working clock configuration, see Section 39.3.71.

   - Enable Timer:
     - Configure APB_SARADC TIMER_EN to enable the timer

   - Data Handling: 
     - When the timer times out, it drives DIG ADC FSM1 to start sampling according to the pattern table.
     - Sample data is automatically stored in memory via DMA. An interrupt is triggered once the scan is completed.

2. **39.3.7.1 DIG ADC Clock**
   - Two clocks can be used as the clock source for DIG ADC1 controller, depending on configuration of APB_SARADC_CLK SEL:
     0: clock off;
     1: Select PLL_D2_CLK as the clock source.
       Then its divided clock DIGADC_CLK is used as working clock for DIG ADC1 controller.

   - Clock Source Configuration (continued):
     2: Select APB_CLK as the clock source
       If DIGADC_CLK is selected, users can configure the divider by APB_SARADC_CLKM_DIV_NUM

   - Note:
     Due to speed limits of SAR ADCs, operating clocks for Digital Reader1 and SAR ADC1 are DIGADC_SARCLK.
     The frequency affects sampling precision. When DIGADC_SARCLK > 5 MHz,
     Sampling Precision is lowered; DIGADC_SARCLK divided from DIGADC_CLK
     Divider coefficient configuration: APB_SARADC_SAR_CLK_DIV

   - Additional Information:
     ADC needs 25 DIGSARCLK clock cycles per sample, so maximum sampling rate limited by DIGSARCLK frequency.

3. **39.3.7.2 DMA Support**
   - DIG ADC1 controller support direct memory access via peripheral DMA.
     Triggered by DIG ADC timer
     Users can switch the DMA data path to DIG ADC by configuring APB_SARADC_APB_ADCTrans via software

**Footer:**
Espressif Systems  
Page 1470 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback