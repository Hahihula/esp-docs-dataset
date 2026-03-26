

```markdown
## 54.3 SD/MMC External Interface Signals

The primary external interface signals, which enable the SD/MMC controller to communicate with an external device, are clock (sdhost_cclk_out_1, eg:card1), command (sdhost_ccmd_out_1), and data signals (sdhost_cdata_in[7:0]/sdhost_cdata_out[7:0]). Additional signals include the card interrupt, card detect, and write protect signals. The direction of each signal is shown in Figure 54.3-1. The direction and description of each pin are listed in Table 54.3-1.

Figure 54.3-1. SD/MMC Controller External Interface Signals

Table 54.3-1. SD/MMC Signal Description

| Signal                  | Direction | Description                     |
|-------------------------|-----------|---------------------------------|
| sdhost_cclk_out         | Output    | Clock signals for slave device  |
| sdhost_ccmd             | Duplex    | Duplex command/response lines   |
| sdhost_cdata            | Duplex    | Duplex data read/write lines    |
| sdhost_card_detect_n    | Input     | Card detection input line       |
| sdhost_card_write_prt   | Input     | Card write protection status input |

## 54.4 Functional Description

### 54.4.1 SD/MMC Host Controller Architecture

The SD/MMC host controller consists of two main functional blocks, as shown in Figure 54.4-1:

* Bus Interface Unit (BIU): Provides the APB interface for registers, access to RAM data, and DMA data read and write operations.
```