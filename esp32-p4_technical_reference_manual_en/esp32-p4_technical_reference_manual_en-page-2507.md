

```markdown
Register 47.2. LP_I2S_RX_CONF_REG (0x0020)

Continued from the previous page...

LP_I2S_RX_SLAVE_MOD    Configures whether to enable slave RX mode.
    0: Disable
    1: Enable
    (R/W)

LP_I2S_RX_FIFOMEM_RESET   Configures whether to reset RX Sync FIFO memory.
    0: No effect
    1: Reset
    (WT)

LP_I2S_RX_MONO    Configures whether to enable RX unit in mono mode.
    0: Disable
    1: Enable
    (R/W)

LP_I2S_RX_BIG_ENDIAN   Configures LP I2S RX byte endian.
    0: Low address data is saved to low address
    1: Low address data is saved to high address
    (R/W)

LP_I2S_RX_UPDATE   Configures whether to update LP I2S RX registers from APB clock domain to LP I2S RX clock domain. This bit will be cleared by hardware after the register update is done.
    0: No effect
    1: Update
    (R/W/SC)

LP_I2S_RX_MONO_FST_VLD   Configures which channel data value is valid in LP I2S RX mono mode.
    0: The second channel data value is valid
    1: The first channel data value is valid
    (R/W)

LP_I2S_RX_STOP_MODE   Configures when LP I2S RX stops data reception.
    0: Only stops when LP_I2S_RX_START is cleared
    1: Stops when LP_I2S_RX_START is cleared or the number of received bytes is greater than the value configured in LP_I2S_RX_EOF_NUM_REG
    Other values: Invalid
    (R/W)

LP_I2S_RX_LEFT_ALIGN   Configures the RX alignment mode.
    0: Right alignment
    1: Left alignment
    (R/W)

Continued on the next page...
```