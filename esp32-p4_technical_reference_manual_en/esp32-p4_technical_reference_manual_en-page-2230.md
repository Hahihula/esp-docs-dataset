

- 0xA (CMDA): only used to generate an SPI_SLV_CMDA_INT interrupt, which will not end GP-SPI's slave segmented transfer.

CMD7, CMD8, CMD9, and CMDA commands are reserved for user definition. These commands can be used as handshake signals, as passwords of some specific functions, as trigger signals of some user defined actions, and so on.

1/2/4-bit modes in states of CMD, ADDR, DATA are supported, which are determined by value of CMD[7:4]. The DUMMY state is always in 1-bit mode and lasts for eight SPI_CLK cycles. The definition of CMD[7:4] is as follows:

- 0x0: CMD, ADDR, and DATA states all are in 1-bit mode.
- 0x1: CMD and ADDR are in 1-bit mode. DATA is in 2-bit mode.
- 0x2: CMD and ADDR are in 1-bit mode. DATA is in 4-bit mode.
- 0x5: CMD is in 1-bit mode. ADDR and DATA are in 2-bit mode.
- 0xA: CMD is in 1-bit mode, ADDR and DATA are in 4-bit mode or in QPI mode.

In addition, if the value of CMD[7:0] is 0x05, 0xA5, 0x06, or 0xDD, DUMMY and DATA states are skipped. The definition of CMD[7:0] is as follows:

- 0x05 (End_SEG_TRANS): master sends this command to end slave segmented transfer in SPI mode.
- 0xA5 (End_SEG_TRANS): master sends this command to end slave segmented transfer in QPI mode.
- 0x06 (En_QPI): GP-SPI enters QPI mode when receiving this command and the bit SPI_QPI_MODE in register SPI_USER_REG is set.
- 0xDD (Ex_QPI): GP-SPI exits QPI mode when receiving this command and the bit SPI_QPI_MODE is cleared.

All the CMD values supported by GP-SPI are listed in Table 43.5-16 and Table 43.5-17. Note that the DUMMY state is always in 1-bit mode and lasts for eight SPI_CLK cycles.

Table 43.5-16. CMD Values Supported in SPI Mode

| Transfer Type | CMD[7:0] | CMD State       | ADDR State      | DATA State     |
|---------------|----------|-----------------|-----------------|----------------|
|               |          |                 |                 |                |
| Wr_BUF        | 0x01     | 1-bit mode      | 1-bit mode      | 1-bit mode     |
|               | 0x11     | 1-bit mode      | 1-bit mode      | 2-bit mode     |
|               | 0x21     | 1-bit mode      | 1-bit mode      | 4-bit mode     |
|               | 0x51     | 1-bit mode      | 2-bit mode      | 2-bit mode     |
|               | 0xA1     | 1-bit mode      | 4-bit mode      | 4-bit mode     |
| Rd_BUF        | 0x02     | 1-bit mode      | 1-bit mode      | 1-bit mode     |
|               | 0x12     | 1-bit mode      | 1-bit mode      | 2-bit mode     |
|               | 0x22     | 1-bit mode      | 1-bit mode      | 4-bit mode     |
|               | 0x52     | 1-bit mode      | 2-bit mode      | 2-bit mode     |
|               | 0xA2     | 1-bit mode      | 4-bit mode      | 4-bit mode     |
| Wr_DMA        | 0x03     | 1-bit mode      | 1-bit mode      | 1-bit mode     |
|               | 0x13     | 1-bit mode      | 1-bit mode      | 2-bit mode     |
|               | 0x23     | 1-bit mode      | 1-bit mode      | 4-bit mode     |
|               | 0x53     | 1-bit mode      | 2-bit mode      | 2-bit mode     |

Espressif Systems
2230
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY