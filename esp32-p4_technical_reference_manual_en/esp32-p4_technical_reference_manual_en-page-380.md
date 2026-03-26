

```markdown
Register 5.14. DMAC_CHn_CFG1_REG (n: 1-4) (0x0100*n) + 0x0124)

| 31 | 30 | 27 | 26 | 23 | 22 | 21 | 20 | 19 | 17 | 16 | 14 | 13 | 12 | 11 | 9 | 8 | 7 | 6 | 3 | 2 | Reset |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|-------|
| 0   | 0x0| 0x0|    | 0x0| 0  |    | 0x3| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0 | 0 | 0 | 0 | 0 | 0x3   |

DMAC_CHn_TT_FC Configures transfer type and flow controller.
- 0x0: Transfer type is memory to memory and flow controller is VDMA
- 0x1: Transfer type is memory to peripheral and flow controller is VDMA
- 0x2: Transfer type is peripheral to memory and flow controller is VDMA
- 0x3: Invalid
- 0x4: Transfer type is peripheral to memory and flow controller is source peripheral
- 0x5: Invalid
- 0x6: Transfer type is memory to peripheral and flow controller is destination peripheral
- 0x7: Invalid (R/W)

DMAC_CHn_SRC_PER Assigns a handshaking interface (0 ~ 2) to the source of channel n. (R/W)

DMAC_CHn_DST_PER Assigns a handshaking interface (0 ~ 2) to the destination of channel n. (R/W)

DMAC_CHn_CH_PRIOR Assigns channel priority (0 ~ 3). A priority of 3 is the highest priority, and 0 is the lowest. A programmed value outside this range will cause erroneous behavior. (R/W)

DMAC_CHn_LOCK_CH VDMA does not support lock feature. Reads of this field always return 0. (RO)

DMAC_CHn_LOCK_CH_L VDMA does not support lock feature. Reads of this field always return 0. (RO)

DMAC_CHn_SRC_OSR_LMT Configures the limit of the source AXI Outstanding request. The maximum number of AXI Outstanding request is 16.
Source AXI Outstanding request limit = Programmed value + 1.
AXI Outstanding is a feature in the AXI protocol that allows to send request before the previous request response is received, thereby increasing the bandwidth of the bus interface. (R/W)

DMAC_CHn_DST_OSR_LMT Configures the limit of the destination AXI Outstanding request. The maximum number of AXI Outstanding request is 16.
Destination AXI Outstanding request limit = Programmed value + 1. (R/W)
```