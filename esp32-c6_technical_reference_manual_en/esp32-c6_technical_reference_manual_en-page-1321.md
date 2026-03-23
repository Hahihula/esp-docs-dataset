

```markdown
Register 37.7. RMT_CHnSTATUS_REG (n: 0-1) (0x0028+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | RMT_APB_MEM_RADDR_CHn                                                     |
| 24  | RMT_APB_MEM_WR_ERR_CHn                                                    |
| 23  | RMT_APB_MEM_EMPTY_CHn                                                     |
| 22  | RMT_APB_MEM_RD_ERR_CHn                                                    |
| 21  | RMT_APB_MEM_WADDR_CHn                                                     |
| 20  |                                                                             |
| 12  | RMT_STATE_CHn                                                              |
| 11  |                                                                             |
| 9   |                                                                             |
| 8   |                                                                             |
| 7-0 | Reset                                                                      |

RMT_MEM_RADDR_EX_CHn Represents the memory address offset when transmitter of channel n is using the RAM. (RO)

RMT_STATE_CHn Represents the FSM status of channel n. (RO)

RMT_APB_MEM_WADDR_CHn Represents the memory address offset when writes RAM over APB bus. (RO)

RMT_APB_MEM_RD_ERR_CHn Represents whether the offset address exceeds memory size when reading via APB bus.
    0: Not exceed
    1: Exceed
    (RO)

RMT_MEM_EMPTY_CHn Represents whether the TX data size exceeds the memory size and the wrap TX mode is disabled.
    0: Not exceed
    1: Exceed
    (RO)

RMT_APB_MEM_WR_ERR_CHn Represents whether the offset address exceeds memory size (overflows) when writes via APB bus.
    0: Not exceed
    1: Exceed
    (RO)

RMT_APB_MEM_RADDR_CHn Represents the memory address offset when reading RAM over APB bus. (RO)
```