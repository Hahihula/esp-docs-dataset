

```markdown
Register 42.7. RMT_CHnSTATUS_REG (n: 0-1) (0x0028+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
| 31  | 0                                                                             |
| 30  | RMT_APB_MEM_WR_ERR_CHn                                                     |
| 29  | RMT_APB_MEM_EMPTY_CHn                                                      |
| 28  | RMT_APB_MEM_RD_ERR_CHn                                                     |
| 27  | RMT_STATE_CHn                                                               |
| 26  | RMT_MEM_RADDR_EX_CHn                                                       |
| 25  | RMT_APB_MEM_WADDR_CHn                                                      |
| 24  | 0                                                                             |
| 23  | 0                                                                             |
| 22  | 0                                                                             |
| 21  | 0                                                                             |
| 20  | 0                                                                             |
| 11  | RMT_APB_MEM_WADDR_CHn                                                      |
| 10  | RMT_STATE_CHn                                                               |
| 9   | RMT_APB_MEM_RD_ERR_CHn                                                     |
| 8   | Reset                                                                        |

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