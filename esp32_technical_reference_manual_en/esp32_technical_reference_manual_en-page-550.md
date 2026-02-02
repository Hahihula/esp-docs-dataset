**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** [GoBack](#)

---

**Table of Registers**

| Name                          | Description                                      | Address         | Access |
|-------------------------------|--------------------------------------------------|-----------------|--------|
| TWAI_CLOCK_DIVIDER_REG       | Clock Divider Register                             | 0x3FF6B07C      | varies |
| Control Registers             |                                                  |                 |        |
| TWAI_CMD_REG                  | Command Register                                  | 0x3FF6B004      | WO     |
| Status Registers               |                                                  |                 |        |
| TWAI_STATUS_REG               | Status Register                                   | 0x3FF6B008      | RO     |
| TWAI_ARB_LOST_CAP_REG         | Arbitration Lost Capture Register                | 0x3FF6B02C      | RO     |
| TWAI_ERR_CODE_CAP_REG         | Error Code Capture Register                       | 0x3FF6B030      | RO     |
| TWAI_RX_ERR_CNT_REG           | Receive Error Counter Register                    | 0x3FF6B038      | RO / R/W|
| TWAI_TX_ERR_CNT_REG           | Transmit Error Counter Register                   | 0x3FF6B03C      | RO / R/W|
| TWAI_RX_MESSAGE_CNT_REG       | Receive Message Counter Register                  | 0x3FF6B074      | RO     |
| Interrupt Registers            |                                                  |                 |        |
| TWAI_INT_RAW_REG              | Interrupt Register                                | 0x3FF6B00C      | RO     |
| TWAI_INT_ENA_REG              | Interrupt Enable Register                        | 0x3FF6B010      | R/W    |

---

**Section Title:**
25.7 Registers

**Body Text:**
The addresses in this section are relative to the TWAI base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **25.6 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

---

**Register Description:**
Register 25.1. TWAI_MODE_REG (0x0000)

| Bit | Name                          |
|-----|-------------------------------|
| 31-0 | (reserved)                    |

TWAI_RESET_MODE
This bit is used to configure the operating mode of the TWAI Controller.
1: Reset mode; 0: Operating mode (R/W)

TWAI_LISTEN_ONLY MODE
1: Listen only mode. In this mode, the nodes will only receive messages from the bus without generating the acknowledge signal nor updating the RX error counter.

TWAI_SELF_TEST_MODE
Self test mode. In this mode, the TX nodes can perform a successful transmission without receiving the acknowledge signal.
This mode is often used to test a single node with the self reception request command (R/W)

TWAI_RX_FILTER_MODE
This bit is used to configure the filter mode:
0: Dual filter mode; 1: Single filter mode

---

**Footer Information:**  
Espressif Systems  
ESP32 TRM (Version 5.6)  

**Page Number and Submission Link:**  
550 Submit Documentation Feedback