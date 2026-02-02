**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**Body Text:**

Counting can be enabled and disabled by setting and clearing TIMGn_Tx_EN. Clearing this bit essentially freezes the counter, causing it to neither count up nor count down; instead, it retains its value until TIMGn_TX_EN is set again. Reloading the counter when TIMGn_TX_EN is cleared will change its value, but counting will not be resumed until TIMGn_TX_EN is set.

Software can set a new counter value by setting registers TIMGn_TX_LOAD_LO and TIMGn_TX_LOAD_HI to the intended new value. The hardware will ignore these register settings until a reload; a reload will cause the contents of these registers to be copied to the counter itself. A reload event can be triggered by an alarm (auto-reload at alarm) or by software (software instant reload). To enable auto-reload at alarm, the register TIMGn_TX_AUTORELOAD should be set. If auto-reload at alarm is not enabled, the time-base counter will continue incrementing or decrementing after the alarm. To trigger a software instant reload, any value can be written to the register TIMGn_TX_LOAD_REG; this will cause the counter value to change instantly. Software can also change the direction of the time-base counter instantly by changing the value of TIMGn_TX_INCREASE.

The time-base counter can also be read by software, but because the counter is 64-bit, the CPU can only get the value as two 32-bit values; the counter value needs to be latched onto TIMGn_TX_LO_REG and TIMGn_TX_HI_REG first. This is done by writing any value to TIMGn_TX_UPDATE_REG; this will instantly latch the 64-bit timer value onto the two registers. Software can then read them at any point in time. This approach stops the timer value being read erroneously when a carry-over happens between reading the low and high word of the timer value.

**Subsections:**

- **10.2.3 Alarm Generation**
  - The timer can trigger an alarm, which can cause a reload and/or an interrupt to occur. The alarm is triggered when the alarm registers TIMGn_TX_ALARMO_REG and TIMGn_TX_ALARMHI_REG match the current timer value. In order to simplify the scenario where these registers are set 'too late' and the counter has already passed these values, the alarm also triggers when the current timer value is higher (for an up-counting timer) or lower (for a down-counting timer) than the current alarm value: if this is the case, the alarm will be triggered immediately upon loading the alarm registers. The timer alarm enable bit is automatically cleared once an alarm occurs.

- **10.2.4 MWDT**
  - Each timer module also contains a Main System Watchdog Timer and its associated registers. While these registers are described here, their functional description can be found in the chapter entitled Watchdog Timer.

- **10.2.5 Interrupts**
  - TIMGn_INT_WDT_INT: Generated when a watchdog timer interrupt stage times out.
  - TIMGn_INT_T1_INT: An alarm event on timer 1 generates this interrupt.
  - TIMGn_INT_TO_INT: An alarm event on timer 0 generates this interrupt.

**Section Title:**
10.3 Register Summary

**Footer Information:**
Espressif Systems
Page number: 224
Document version and submission information:
ESP32 TRM (Version 5.6)
Submit Documentation Feedback