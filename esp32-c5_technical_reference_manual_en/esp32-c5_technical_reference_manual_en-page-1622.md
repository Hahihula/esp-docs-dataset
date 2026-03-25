

```markdown
## 42.7 Registers

The addresses in this section are relative to Remote Control Peripheral base address provided in Table 6.3-2 in Chapter 6 System and Memory.

Register 42.1. RMT_CHnDATA_REG (n: 0-3) (0x0000+0x4*n)

| Bit | Description |
|-----|-------------|
| 31  | RMT_CHnDATA |
|     |             |
| 0   | Reset       |

RMT_CHnDATA Read and write data for channel n via APB FIFO. (HRO)

Register 42.2. RMT_CHnCONFO_REG (n: 0-1) (0x0010+0x4*n)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 25  | RMT_CONF_UPDATE_CHn (reset) |
| 24  | RMT_CARRIER_OUT_LV_CHn |
| 23  | RMT_CARRIER_EN_CHn |
| 22  | RMT_CARRIER_EFF_ENL_CHn |
| 21  | RMT_MEM_SIZE_CHn |
| 20  | (reserved) |
| 19  | RMT_DIV_ONT_CHn |
| 18  | RMT_TX_STOP_CHn |
| 17  | RMT_IDLE_OUT_EN_LV_CHn |
| 16  | RMT_IDLE_OUT_EN_CHn |
| 15  | RMT_WRAP_EN_CHn |
| 14  | RMT_CONT_MODE_CHn |
| 13  | RMT_APB_MEM_RST_CHn |
| 12  | RMT_TX_RD_RST_CHn |
| 11  | RMT_TX_START_CHn |
| 10  | Reset       |

RMT_TX_START_CHn Configures whether to enable sending data in channel n.
O: No effect
1: Enable (WT)

RMT_MEM_RD_RST_CHn Configures whether to reset RAM read address accessed by the transmitter for channel n.
O: No effect
1: Reset (WT)

RMT_APB_MEM_RST_CHn Configures whether to reset RAM W/R address accessed by APB FIFO for channel n.
O: No effect
1: Reset (WT)

Continued on the next page...
```