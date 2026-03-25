

```markdown
Chapter 42 Remote Control Peripheral (RMT)

Register 42.4. RMT_CHmCONF1_REG (m: 2-3) (0x001C+0x8*(m-2))

Continued from the previous page...

RMT_MEM_OWNER_CHm Configures the ownership of channel m's RAM block.
    0: APB bus is using the RAM
    1: Receiver is using the RAM
        (R/W/SC)

RMT_RX_FILTER_EN_CHm Configures whether to enable the receiver's filter for channel m.
    0: Disable
    1: Enable
        (R/W)

RMT_RX_FILTER_THRES_CHm Configures whether the receiver, when receiving data, ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles.
    0: No effect
    1: Reset
        (R/W)

RMT_MEM_RX_WRAP_EN_CHm Configures whether to enable wrap RX mode for channel m.
    0: Disable
    1: Enable
        In this mode, if the RX data size is larger than channel m's RAM block size, the receiver stores the RX data from the first address to the last address in loops.
        (R/W)

RMT_CONF_UPDATE_CHm Synchronization of RMT Channel m. (WT)

Register 42.5. RMT_SYS_CONF_REG (0x0068)
```

```markdown
| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | 30                 | (reserved)                                                                   |
|     |                    |                                                                             |
| 0   | RMT_APB_FIFO_MASK | Configures the memory access mode.                                         |
|     |                    | 0: Access memory by FIFO                                                    |
|     |                    | 1: Access memory directly                                                   |
|     |                    | (R/W)                                                                        |
| 0   | RMT_CLK_EN         | Configures whether to enable signal of RMT register clock gate.              |
|     |                    | 0: Power down the drive clock of registers                                   |
|     |                    | 1: Power up the drive clock of registers                                    |
|     |                    | (R/W)                                                                        |

Espressif Systems    1626
ESP32-C5 TRM (Version 1.0)
```