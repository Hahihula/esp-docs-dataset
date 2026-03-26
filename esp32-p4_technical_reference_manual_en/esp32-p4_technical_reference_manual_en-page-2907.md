
```markdown
Register 57:10. RMT_CHmSTATUS_REG (m: 4-7) (0x0050+0x4*m)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |    |    |    |    |    |    |    |    |    |
|     |    |    |    |    |    |    |    |    |    |    | RMT_STATE_CHm | RMT_MEM_OWNER_ERR_CHm | RMT_MEM_FULL_CHm | RMT_APB_MEM_RD_ERR_CHm | RMT_APB_MEM_RADDR_CHm | RMT_MEM_WADDR_EX_CHm |
| Reset Value | 0x00 | 0xC0 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
```

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