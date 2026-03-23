

```markdown
Chapter 28 SPI Controller (SPI)

Register 28.3. SPI_USER_REG (0x0010)
```

Continued from the previous page...

```markdown
SPI_CK_OUT_EDGE Configures SPI clock mode together with SPI_CK_IDLE_EDGE. (R/W)
Can be configured in CONF state. For more information, see Section 28.7.2.
```

```markdown
SPI_FWRITE_DUAL Configures whether or not to enable the 2-bit mode of read-data phase in write operations. (R/W)

- O: Not enable
- 1: Enable

Can be configured in CONF state.
```

```markdown
SPI_FWRITE_QUAD Configures whether or not to enable the 4-bit mode of read-data phase in write operations. (R/W)

- O: Not enable
- 1: Enable

Can be configured in CONF state.
```

```markdown
SPI_USR_CONF_NXT Configures whether or not to enable the CONF state for the next transaction (segment) in a configurable segmented transfer. (R/W)

- O: this transfer will end after the current transaction (segment) is finished. Or this is not a configurable segmented transfer.
- 1: this configurable segmented transfer will continue its next transaction (segment).

Can be configured in CONF state.
```

```markdown
SPI_SIO Configures whether or not to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin. (R/W)

- O: Disable
- 1: Enable

Can be configured in CONF state.
```

```markdown
SPI_USR_MISO_HIGHPART Configures whether or not to enable "high part mode", i.e., only access to high part of the buffers: SPI_W8_REG ~ SPI_W15_REG in read-data phase. (R/W)

- O: Disable
- 1: Enable

Can be configured in CONF state.
```

Continued on the next page...
```