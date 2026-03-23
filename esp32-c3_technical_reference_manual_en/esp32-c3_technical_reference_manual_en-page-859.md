

Chapter 33 Remote Control Peripheral (RMT)

Register 339. RMT_CHmSTATUS_REG (m = 2, 3) (0x0030, 0x0034)

| 31 | 28 | 27 | 26 | 25 | 24 | 22 | 21 | 20 | 12 | 11 | 9 | 8 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|---|---|---|
| 0  | 0  | 0  | 0  | 0  | 0  | 0  |    |    | 0  | 0  | 0 |    | Reset |

RMT_MEM_WADDR_EX_CHm This field records the memory address offset when the receiver of channel m is using the RAM. (RO)

RMT_APB_MEM_RADDR_CHm This field records the memory address offset when reads RAM over APB bus. (RO)

RMT_STATE_CHm This field records the FSM status of channel m. (RO)

RMT_MEM_OWNER_ERR_CHm This status bit will be set when the ownership of memory block is wrong. (RO)

RMT_MEM_FULL_CHm This status bit will be set if the receiver receives more data than the memory can fit. (RO)

RMT_APB_MEM_RD_ERR_CHm This status bit will be set if the offset address is out of memory size (overflows) when reads RAM via APB bus. (RO)