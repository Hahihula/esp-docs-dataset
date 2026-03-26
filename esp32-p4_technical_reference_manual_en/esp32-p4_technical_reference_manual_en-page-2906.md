

```markdown
Register 57.9. RMT_CHn_STATUS_REG (n: 0-3) (0x0050+0x4*n)

| 31 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 11 | 10 | 9 | Reset |
|----|----|----|----|----|----|----|----|----|----|----|---|-------|
| 0  | 0  | 0  | 0  | 0  | 0  | 0  |    |    | 0  | 0  | 0   |       |

RMT_MEM_RADDR_EX_CHn Represents the memory address offset when transmitter of channel n is using the RAM. (RO)

RMT_APB_MEM_WADDR_CHn Represents the memory address offset when writes RAM over APB bus. (RO)

RMT_STATE_CHn Represents the FSM status of channel n. (RO)

RMT_MEM_EMPTY_CHn Represents whether the TX data size exceeds the memory size and the wrap TX mode is disabled.
O: Not exceed
1: Exceed
(RO)

RMT_APB_MEM_WR_ERR_CHn Represents whether the offset address exceeds memory size (overflows) when writes via APB bus.
O: Not exceed
1: Exceed
(RO)
```