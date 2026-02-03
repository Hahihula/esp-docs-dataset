**Chapter 37: Remote Control Peripheral (RMT)**

---

2. **RMT can only start sending data after DMA channel gets data ready, otherwise, unexpected data may be sent.**

   - In normal TX mode, when the RAM of channel 3 is fully written by DMA, an RMT_APB_MEM_WR_ERR_CH3 interrupt is triggered. Setting `RMT_MEM_TX.WRAP_EN_CH3` allows channel 3 to transmit more data than one block can fit, with no software operation needed.
   
   - Channel 7 also supports DMA access. If `RMT_DMA_ACCESS_EN_CH7` is set, the RAM of channel 7 is allowed to send data to DMA. Note in this mode, channel 7’s RAM can also be accessed by APB via NONFIFO mode.

   - In normal RX mode, when the size of data read by DMA from channel 7 is equal to its RAM size, an `RMT_APB_MEM_RD_ERR_EN_CH7` is triggered and the subsequent data is discarded. If `RMT_MEM_RX.WRAP_EN_CH7` set, data more than one block size can be received with no software wrap operation needed. If channel 7’s RAM is full but the DMA still does not start receiving data from the channel, the newly received data by this channel will replace the previous data.

**Note:**
When channel 7 receives an end-maker, a DMA in _suc_eof_ interrupt is generated. Two bytes are written to DMA if the period[14:0] is 0, and four bytes to DMA if the period[30:16] is 0.

---

### **37.3.3 Clock**

The clock source of RMT can be APB_CLK, RC_FAST_CLK, or XTAL_CLK, depending on the configuration of `RMT_SCLK_SEL`. RMT clock can be enabled by setting `RMT_SCLK_ACTIVE`. RMT working clock is obtained by dividing the selected clock source with a fractional divider. See Figure 37.3-1.

The divider is:

```
RMT_SCLK_DIV_NUM + 1 + RMT_SCLK_DIV_A/RMT_SCLK_DIV_B
```

For more information, see Chapter 7 Reset and Clock. `RMT_DIV_CNT_CHn/m` used to configure the divider coefficient of internal clock divider for RMT channels. The coefficient is normally equal to the value of `RMT_DIV_CNT_CHn/m`, except value 0 that represents divider 256. The clock divider can be reset by setting `RMT_REF_CNT_RST_CHn/m`. The clock generated from the divider can be used by the counter (see Figure 37-1).

---

### **37.3.4 Transmitter**

**Note:**
Updating the configuration described in this and subsequent sections requires to set `RMT_CONF_UPDATE_CHn` first, see Section 37.3.6.

---

### **37.3.4.1 Normal TX Mode**

When `RMT_TX_START_CHn` is set, the transmitter of channel _n_ starts reading and sending pulse codes from the starting address of its RAM block. The codes are sent starting from low-address entry. When an end-marker (a zero period) is encountered, the transmitter stops the transmission, returns to idle state and generates an `RMT_CHn_TX_END_INT`. Setting `RMT_TX_STOP_CHn` to 1 also stops the transmission.

---

**Espressif Systems**

**Page Number:**
1419

**Document Version:** 
ESP32-S3 TRM (Version 1.7)

**Submit Documentation Feedback**