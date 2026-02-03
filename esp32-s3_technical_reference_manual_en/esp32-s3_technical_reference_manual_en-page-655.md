**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Heading:**
12.2 Functional Description

**Figure Caption and Image Description:**
- Figure caption: "Figure 12.2-1. Timer Group Architecture"
- The image is a diagram of timer Tx in a timer group, showing various components such as Clock, TIMG_Tx_DIVIDER, TIMG_Tx_EN, TIMG_Tx_INCREASE, TIMG_Tx_ALARM_EN, Int Divider (16 bits), Inc/Dec Counter, TIMG_VALUE, ALARM_VALUE, Comparator, and TIMG_Tx_USE_XTAL.

**Subsection Title:**
12.2.1 16-bit Prescaler and Clock Selection

**Body Text for Subsection:**
Each timer can select between the APB clock (APB_CLK) or external clock (XTAL_CLK) as its clock source by setting the TIMG_Tx_USE_XTAL field of the TIMG_Tx_CONFIG_REG register. The clock is then divided by a 16-bit prescaler to generate the time-base counter clock (TB_CLK) used by the time-base counter. When the TIMG_Tx_DIVIDER field is configured as 2 ~ 65536, the divisor of the prescaler would be 2 ~ 65536. Note that programming value 0 to TIMG_Tx_DIVIDER will result in the divisor being 65536. When the prescaler is set to 1, the actual divisor is 2, so the time-counter value represents half of real time.

Before you modify the 16-bit prescaler, the timer must be disabled (i.e., TIMG_Tx_EN should be cleared). Otherwise, the result can be unpredictable.

**Subsection Title:**
12.2.2 54-bit Time-base Counter

**Body Text for Subsection:**
The 54-bit time-base counters are based on TB_CLK and can be configured to increment or decrement via the TIMG_Tx_INCREASE field. The time-base counter can be enabled or disabled by setting or clearing the TIMG_Tx_EN field, respectively. When enabled, the time-base counter increments or decrements on each cycle of TB_CLK. When disabled, the time-base counter is essentially frozen. Note that the TIMG_Tx_INCREASE field can be changed while TIMG_Tx_EN is set and this will cause the time-base counter to change direction instantly.

To read the 54-bit value of the time-base counter, the timer value must be latched to two registers before being read by the CPU (due to the CPU being 32-bit). By writing any value to the TIMG_TxUPDATE_REG and TIMG_TxHI_REG, the current value of the 54-bit timer starts to be latched into the TIMG_TxLO_REG. When TIMG_TxUPDATE_REG is cleared by hardware, it indicates the latch operation has been completed and current time value can be read from the TIMG_TxLO_REG and TIMG_TxHI_REG registers. TIMG_TxLO_REG and TIMG_TxHI_REG registers will remain unchanged for the CPU to read in its own time until TIMG_TxUPDATE_REG is written to again.

**Footer:**
Espressif Systems
655 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback