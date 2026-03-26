

```markdown
|31|29|28|27|26| | | | |15|14|12|11|9|8|6|5|3|2|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|0| | | | | | | | | | | | | | | | | |
|| ||||||||||||||
||Reset|
```

### AHB_DMA_AHB_APB_SYNC_CLK_EN
Configures whether to forcibly enable the clock for the AHB DMA register configuration synchronization module.
Bit 0 corresponds to TX and RX channel 0, bit 1 corresponds to channel TX and RX 1, and so on.

- O: Not forcibly enable
- 1: Forcibly enable

(R/W)

### AHB_DMA_OUT_DSCR_CLK_EN
Configures whether to forcibly enable the clock for the AHB DMA TX descriptor processing module.
Bit 0 corresponds to TX channel 0, bit 1 corresponds to TX channel 1, and so on.

- O: Not forcibly enable
- 1: Forcibly enable

(R/W)

### AHB_DMA_OUT_CTRL_CLK_EN
Configures whether to forcibly enable the clock for the AHB DMA TX data processing module.
Bit 0 corresponds to TX channel 0, bit 1 corresponds to TX channel 1, and so on.

- O: Not forcibly enable
- 1: Forcibly enable

(R/W)

### AHB_DMA_IN_DSCR_CLK_EN
Configures whether to forcibly enable the clock for the AHB DMA RX descriptor processing module.
Bit 0 corresponds to RX channel 0, bit 1 corresponds to TX channel 1, and so on.

- O: Not forcibly enable
- 1: Forcibly enable

(R/W)

### AHB_DMA_IN_CTRL_CLK_EN
Configures whether to forcibly enable the clock for the AHB DMA RX data processing module.
Bit 0 corresponds to RX channel 0, bit 1 corresponds to TX channel 1, and so on.

- O: Not forcibly enable
- 1: Forcibly enable

(R/W)

Continued on the next page...
```