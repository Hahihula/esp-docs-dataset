

```markdown
Register 42.8. RMT_CHm_STATUS_REG (m: 2-3) (0x0030+0x4*(m-2))

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|
|     |    |    |    | (reserved) | RMT_APB_MEM_RD_ERR_CHm | RMT_MEM_OWNER_ERR_CHm | RMT_MEM_FULL_CHm | RMT_STATE_CHm | (reserved) | RMT_APB_MEM_RADDR_CHm | RMT_MEM_WADDR_EX_CHm | 0 | Reset |
|     |    |    |    |              |                         |                     |                 |               |                  |                       |                   |   |      |

RMT_MEM_WADDR_EX_CHm Represents the memory address offset when receiver of channel m is using the RAM. (RO)

RMT_APB_MEM_RADDR_CHm Represents the memory address offset when reads RAM over APB bus. (RO)

RMT_STATE_CHm Represents the FSM status of channel m. (RO)

RMT_MEM_OWNER_ERR_CHm Represents whether the ownership of memory block is wrong.
0: The ownership of memory block is correct
1: The ownership of memory block is wrong
(RO)

RMT_MEM_FULL_CHm Represents whether the receiver receives more data than the memory can fit.
0: The receiver does not receive more data than the memory can fit
1: The receiver receives more data than the memory can fit
(RO)

RMT_APB_MEM_RD_ERR_CHm Represents whether the offset address exceeds memory size (overflows) when reads RAM via APB bus.
0: Not exceed
1: Exceed
(RO)
```