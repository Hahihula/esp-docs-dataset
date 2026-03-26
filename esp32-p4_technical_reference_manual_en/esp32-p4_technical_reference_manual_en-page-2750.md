

```markdown
Register 54.7. SDHOST_BLKSIZ_REG (0x001C)

SDHOST_BLOCK_SIZE Configures the Block Size. (R/W)


Register 54.8. SDHOST_BYTCNT_REG (0x0020)

SDHOST_BYTE_COUNT Configures the number of bytes to be transferred, should be an integral multiple of Block Size for block transfers. For data transfers of undefined byte lengths, the byte count should be set to 0. When the byte count is set to 0, it is the responsibility of the host to explicitly send a stop/abort command to terminate data transfer. (R/W)


Register 54.9. SDHOST_CMDARG_REG (0x0028)

SDHOST_CMDARG_REG Configures the value indicates the command argument to be passed to the card. (R/W)
```