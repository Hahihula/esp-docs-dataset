

```markdown
Register 33.8. RMT_CHnSTATUS_REG (n = 0, 1) (0x0028, 0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0x0                                                                          |
| 31  | Reset                                                                       |
| 24  | 0                                                                           |
| 23  | 0                                                                           |
| 22  | 0                                                                           |
| 21  | 0                                                                           |
| 20  | 0                                                                           |
| 12  | 0                                                                           |
| 11  | 0                                                                           |
| 9   | 0                                                                           |
| 8   | 0                                                                           |

RMT_MEM_RADDR_EX_CHn This field records the memory address offset when transmitter of channel n is using the RAM. (RO)

RMT_STATE_CHn This field records the FSM status of channel n. (RO)

RMT_APB_MEM_WADDR_CHn This field records the memory address offset when writes RAM over APB bus. (RO)

RMT_APB_MEM_RD_ERR_CHn This status bit will be set if the offset address is out of memory size (overflows) when reads RAM via APB bus. (RO)

RMT_MEM_EMPTY_CHn This status bit will be set when the TX data size is larger than the memory size and the wrap TX mode is disabled. (RO)

RMT_APB_MEM_WR_ERR_CHn This status bit will be set if the offset address is out of memory size (overflows) when writes via APB bus. (RO)

RMT_APB_MEM_RADDR_CHn This field records the memory address offset when reads RAM over APB bus. (RO)
```