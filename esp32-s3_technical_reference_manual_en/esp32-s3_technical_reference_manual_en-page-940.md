**Title: Chapter 26 UART Controller (UART)**

---

### Table of Contents:
- **Table 26.5-1 – cont’d from previous page**
- Section Title: Static Registers 
- Subtitle: Table 26.5-2 Static Registers 

---

#### Table 26.5-1
| Register | Field |
|----------|-------|
| UART_FLOW_CONF_REG | UART_SEND_XOFF |
| | UART_SEND_XON |
| | UART_FORCE_XOFF |
| | UART FORCE XON |
| | UART_XONOFF_DEL |
| | UART SW FLOW CONN_EN |
| | UART_RS485_TX_DLY_NUM[3:0] |
| | UART_RS485_RX_DLY_NUM |
| | UART RS485RXBY_TX_EN |
| | UART RS485TX_RX_EN |
| | UART DL1_EN |
| | UART DLO_EN |
| | UART_RS485_EN |

---

#### Section 26.5.1.2 Static Registers

Static registers, though also read in Core Clock domain, would not change dynamically when UART controllers are at work; so they do not implement the clock domain crossing design. These registers must be configured when the UART transmitter or receiver is not at work.

In this case, software can turn off the clock for the UART transmitter or receiver to prevent static registers from being sampled in their metastable state.
When software turns on the clock, the configured values are stable and correctly sampled.


Static registers as listed in Table 26.5-2

##### Instructions:
1. Turn off the clock for the UART transmitter by clearing `UART_TX_SCLK_EN`, or the clock for the UART receiver by clearing `UART_RX_SCLK_EN`, depending on which one (transmitter or receiver) is not at work;
2. Configure static registers;
3. Turn on the clock for the UART transmitter by writing 1 to `UART_TX_SCLK_EN`, or the clock for the UART receiver by writing 1 to `UART_RX_SCLK_EN`.

---

#### Table 26.5-2
| Register | Field |
|----------|-------|
| UART_RX_FILT_REG | UART_GLITCH_FILT_EN |
| | UART_GLITCH_FILT[7:0] |
| UART_SLEEP_CONF_REG | UART_ACTIVE_THRESHOLD[9:0] |
| | UART SWFC_INFO_REG |
| | UART_XON_XOFF[7:0] |
| | UART SWFC_CONF1_REG |
| | UART_XON_XON[7:0] |
| | UART_IDLE_CONF_REG | UART_TX_IDLE_NUM[9:0] |
| | UART_AT_CMD_PRECNT_REG | UART_PRE_IDLE_NUM[15:0] |
| | UART_AT_CMD_POSTCNT_REG | UART_POST_IDLE_NUM[15:0] |
| | UART_AT_CMD_GAPOUT_REG | UART_RX_GAP_TOUT[7:0] |
| | UART_AT_CMD_CHAR_REG | UART CHAR_NUM[7:0] |

---

**Footer:** Espressif Systems  
940 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback