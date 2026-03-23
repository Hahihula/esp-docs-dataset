

```markdown
Register 30.5. I2S_RX_CONF_REG (0x0020)

I2S_RX_RESET   Configures whether to reset RX unit.
               O: No effect
               1: Reset
               (WT)

I2S_RX_FIFO_RESET   Configures whether to reset RX FIFO.
                    O: No effect
                    1: Reset
                    (WT)

I2S_RX_START   Configures whether to start receiving data.
               O: No effect
               1: Start
               (R/W/SC)

I2S_RX_SLAVE_MOD   Configures whether to enable slave RX mode.
                   O: Disable
                   1: Enable
                   (R/W)

I2S_RX_MONO   Configures whether to enable RX unit in mono mode.
              O: Disable
              1: Enable
              (R/W)

I2S_RX_BIG_ENDIAN   Configures I2S RX byte endian.
                    O: Low address data is saved to low address
                    1: Low address data is saved to high address
                    (R/W)

I2S_RX_UPDATE   Configures whether to update I2S RX registers from APB clock domain to I2S RX clock domain.
                O: No effect
                1: Update
                This bit will be cleared by hardware after the register update is done.
                (R/W/SC)
```