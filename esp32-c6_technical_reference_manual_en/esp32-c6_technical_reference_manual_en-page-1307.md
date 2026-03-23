

```markdown
configured to designate the RAM block's owner, be it the receiver or the APB bus, by configuring RMT_MEM_OWNER_CHm. If this ownership is violated, a flag signal RMT_MEM_OWNER_ERR_CHm will be generated.

When the RMT module is inactive, the RAM can be put into low-power mode by setting RMT_MEM_FORCE_PD.
```

```markdown
37.3.2.3 RAM Access

APB bus is able to access RAM in FIFO mode and in NONFIFO (Direct Address) mode, depending on the configuration of RMT_APB_FIFO_MASK:

*   0: use FIFO mode;
*   1: use NONFIFO mode.
```

```markdown
FIFO Mode

In FIFO mode, the APB reads data from or writes data to RAM via a fixed address stored in RMT_CHn/mDATA_REG.

NONFIFO Mode

In NONFIFO mode, the APB writes data to or reads data from a continuous address range.

*   The write-starting address of TX channel n is: RMT base address + 0x400 + (n - 1) x 48. The access address for the second data and the following data are RMT base address + 0x400 + (n - 1) x 48 + 0x4, and so on, incremented by 0x4.
*   The read-starting address of RX channel m is: RMT base address + 0x460 + (m - 1) x 48. The access address for the second data and the following data are RMT base address + 0x460 + (m - 1) x 48 + 0x4, and so on, incremented by 0x4.
```

```markdown
37.3.3 Clock

The clock source of RMT can be PLL_F8OM_CLK, RC_FAST_CLK, or XTAL_CLK, depending on the configuration of PCR_RMT_SCLK_SEL. RMT clock can be enabled by setting PCR_RMT_SCLK_EN. RMT working clock (see rmt_sclk in Figure 37.3-1) is obtained by dividing the selected clock source with a fractional divider. The divider is:

PCR_RMT_SCLK_DIV_NUM + 1 + PCR_RMT_SCLK_DIV_A / PCR_RMT_SCLK_DIV_B

For more information, see Chapter 8 Reset and Clock. RMT_DIV_CNT_CHn/m is used to configure the divider coefficient of internal clock divider for RMT channels. The coefficient is normally equal to the value of RMT_DIV_CNT_CHn/m, except for value 0 that represents divider 256. The clock divider can be reset by setting RMT_REF_CNT_RST_CHn/m. The clock generated from the divider can be used by the counter (see Figure 37.3-1).
```

```markdown
37.3.4 Transmitter

Espressif Systems	1307	ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```