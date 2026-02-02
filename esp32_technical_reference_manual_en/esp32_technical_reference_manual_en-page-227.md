Title: Chapter 10 Timer Group (TIMG)

Subtitle: GoBack

Section Title: 10.4 Registers

Body Text:
The addresses in parenthesis besides register names are the register addresses relative to the TIMG base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 10.3 Register Summary.

Figure Caption: Register Table
- Register Name (TIMGn_Tx CONFIG_REG): x (0-1) (0x0+0x24*x)
- Description of bits:
  - TIMGn_Tx_EN: When set, the timer time-base counter is enabled.
  - TIMGn_Tx_INCREASE: When set, the timer time-base counter will increment every clock tick. 
    - Note: When cleared, the time-base counter will decrement (R/W).
  - TIMGn_Tx_AUTORELOAD: When set, timer auto-reload at alarm is enabled.
  - TIMGn_Tx_DIVIDER: Timer clock (Tx_clk) prescale value.

- Other registers listed with their descriptions:
  - TIMGn_Tx_EDGE_INT_EN
  - TIMGn_Tx_LEVEL_INT_EN
  - TIMGn_Tx_ALARM_EN

Another Register Table Captioned as "Register 10.2."
- Register Name (TIMGn_Tx LO_REG): x (0-1) (0x4+0x24*x)
- Description: After writing to TIMGn_Tx UPDATE_REG, the low 32 bits of the time-base counter of timer can be read here.

Another Register Table Captioned as "Register 10.3."
- Register Name (TIMGn_Tx HI_REG): x (0-1) (0x8+0x24*x)
- Description: After writing to TIMGn_Tx UPDATE_REG, the high 32 bits of the time-base counter can be read here.

Footer:
Espressif Systems
Submit Documentation Feedback

Page Number and Document Version Information at Bottom Right Corner:

ESP32 TRM (Version 5.6)