

```markdown
Chapter 16 Timer Group (TIMG)

GoBack

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 16.5 Register Summary.

16.4 Configuration and Usage

16.4.1 Timer as a Simple Clock

1. Configure the time-base counter
   - Select clock source by configuring the HP_SYS_CLKRST_TIMERGRO_TGRT_CLK_SRC_SEL field of the HP_SYS_CLKRST_PERI_CLK_CTRL21_REG register.
   - Configure the 16-bit prescaler by setting TIMG_Tx_DIVIDER.
   - Configure the timer direction by setting or clearing TIMG_Tx_INCREASE.
   - Set the timer’s starting value by writing the starting value to TIMG_Tx_LOAD_LO and TIMG_Tx_LOAD_HI, then reloading it into the timer by writing any value to TIMG_TxLOAD_REG.

2. Start the timer by setting TIMG_Tx_EN.

3. Get the timer’s current value.
   - Write any value to TIMG_TxUPDATE_REG to latch the timer’s current value.
   - Wait until TIMG_TxUPDATE_REG is cleared by hardware.
   - Read the latched timer value from TIMG_TxLO_REG and TIMG_TxHI_REG.

16.4.2 Timer as One-shot Alarm

1. Configure the time-base counter following step 1 of Section 16.4.1.
2. Configure the alarm.
   - Configure the alarm value by setting TIMG_TxALARMLO_REG and TIMG_TxALARMIHI_REG.
   - Enable interrupt by setting TIMG_Tx_INT_ENA.

3. Disable auto reload by clearing TIMG_Tx_AUTORELOAD.

4. Start the alarm by setting TIMG_Tx_ALARM_EN.

5. Handle the alarm interrupt.
   - Clear the interrupt by setting the timer’s corresponding bit in TIMG_Tx_INT_CLR.
   - Disable the timer by clearing TIMG_Tx_EN.

16.4.3 Timer as Periodic Alarm by APB

1. Configure the time-base counter following step 1 in Section 16.4.1.
2. Configure the alarm following step 2 in Section 16.4.2.
3. Enable auto reload by setting TIMG_Tx_AUTORELOAD and configure the reload value via TIMG_Tx_LOAD_LO and TIMG_Tx_LOAD_HI.

Espressif Systems
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```