

```markdown
| Name | Description | Address | Access |
|:-------------------------------|:------------------------------------------|:---------|:--------|
| **Configuration Registers** |  |  |  |
| TWAI_MODE_REG | Mode Register | 0x0000 | R/W |
| TWAI_BUS_TIMING_O_REG | Bus Timing Register 0 | 0x0018 | RO | R/W |
| TWAI_BUS_TIMING_1_REG | Bus Timing Register 1 | 0x001C | RO | R/W |
| TWAI_ERR_WARNING_LIMIT_REG | Error Warning Limit Register | 0x0034 | RO | R/W |
| TWAI_DATA_O_REG | Data Register 0 | 0x0040 | WO | R/W |
| TWAI_DATA_1_REG | Data Register 1 | 0x0044 | WO | R/W |
| TWAI_DATA_2_REG | Data Register 2 | 0x0048 | WO | R/W |
| TWAI_DATA_3_REG | Data Register 3 | 0x004C | WO | R/W |
| TWAI_DATA_4_REG | Data Register 4 | 0x0050 | WO | R/W |
| TWAI_DATA_5_REG | Data Register 5 | 0x0054 | WO | R/W |
| TWAI_DATA_6_REG | Data Register 6 | 0x0058 | WO | R/W |
| TWAI_DATA_7_REG | Data Register 7 | 0x005C | WO | R/W |
| TWAI_DATA_8_REG | Data Register 8 | 0x0060 | WO | RO |
| TWAI_DATA_9_REG | Data Register 9 | 0x0064 | WO | RO |
| TWAI_DATA_10_REG | Data Register 10 | 0x0068 | WO | RO |
| TWAI_DATA_11_REG | Data Register 11 | 0x006C | WO | RO |
| TWAI_DATA_12_REG | Data Register 12 | 0x0070 | WO | RO |
| TWAI_CLOCK_DIVIDER_REG | Clock Divider Register | 0x007C | varies |
| **Contro Registers** |  |  |  |
| TWAI_CMD_REG | Command Register | 0x0004 | WO |
| **Status Register** |  |  |  |
| TWAI_STATUS_REG | Status Register | 0x0008 | RO |
| TWAI_ARB LOST CAP_REG | Arbitration Lost Capture Register | 0x002C | RO |
| TWAI_ERR_CODE_CAP_REG | Error Code Capture Register | 0x0030 | RO |
| TWAI_RX_ERR_CNT_REG | Receive Error Counter Register | 0x0038 | RO | R/W |
| TWAI_TX_ERR_CNT_REG | Transmit Error Counter Register | 0x003C | RO | R/W |
| TWAI_RX_MESSAGE_CNT_REG | Receive Message Counter Register | 0x0074 | RO |
| **Interrupt Registers** |  |  |  |
| TWAI_INT_RAW_REG | Interrupt Register | 0x000C | RO |
| TWAI_INT_ENA_REG | Interrupt Enable Register | 0x0010 | R/W |
```