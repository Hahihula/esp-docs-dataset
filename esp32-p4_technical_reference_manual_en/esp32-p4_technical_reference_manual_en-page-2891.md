

```markdown
GoBack

GDMA Mode

Channel 3 also supports GDMA access. If RMT_DMA_ACCESS_EN_CH3 is set, RAM of channel 3 only allows GDMA access. FIFO access or NOFIFO access to channel 3 by the APB bus are forbidden, otherwise unpredictable consequences may occur.

To ensure correct data transmission,

1. GDMA should be started first.
2. RMT can only start transmitting data after GDMA channel gets data ready, otherwise, unexpected data may be sent.

In normal TX mode, when the RAM of channel 3 is fully written by GDMA, an RMT_APB_MEM_WR_ERR_CH3 interrupt is triggered. Setting RMT_MEM_TX_WRAP_EN_CH3 allows channel 3 to transmit more data than one block can fit, with no software operation needed.

Channel 7 also supports GDMA access. If RMT_DMA_ACCESS_EN_CH7 is set, the RAM of channel 7 is allowed to transmit data to GDMA. Note in this mode, channel 7's RAM can also be accessed by APB via NONFIFO mode.

In normal RX mode, when the size of data read by GDMA from channel 7 is equal to its RAM size, an RMT_APB_MEM_RD_ERR_CH7 is triggered and the subsequent data is discarded. If RMT_MEM_RX_WRAP_EN_CH7 is set, data of more than one block size can be received with no software wrap operation needed. If channel 7's RAM is full but the GDMA still does not start receiving data from the channel, the newly received data by this channel will replace the previous data.

Note:
When channel 7 receives an end-maker, a GDMA in_succ_eof interrupt is generated. Two bytes are written to GDMA if the period[14:0] is 0, and four bytes to GDMA if the period[30:16] is 0.

57.3.3 Clock

The clock source of RMT can be PLL_F80M_CLK, RC_FAST_CLK, or XTAL_CLK, depending on the configuration of HP_SYS_CLKRST_RMT_CLK_SRC_SEL. RMT clock can be enabled by setting HP_SYS_CLKRST_RMT_CLK_EN. RMT working clock (see rmt_sclk in Figure 57.3-1) is obtained by dividing the selected clock source with a fractional divider. The divider is

HP_SYS_CLKRST_RMT_CLK_DIV_NUM + 1 + HP_SYS_CLKRST_RMT_CLK_DIV_NUMERATOR or
HP_SYS_CLKRST_RMT_CLK_DIV_DENOMINATOR.

For more information, see Chapter 10 Reset and Clock. RMT_DIV_CNT_CHn/m is used to configure the divider coefficient of internal clock divider for RMT channels. The coefficient is normally equal to the value of RMT_DIV_CNT_CHn/m, except value 0 that represents divider 256. The clock divider can be reset by setting RMT_REF_CNT_RST_CHn/m. The clock generated from the divider can be used by the counter (see Figure 57.3-1).

57.3.4 Transmitter
```