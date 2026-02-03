**Title: Chapter 21 HMAC Accelerator (HMAC)**

**GoBack**

| Name                          | Description                                                                                   | Address   | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|----------|--------|
| HMAC_RD_RESULT_5_REG         | Hash result register 5                                                                      | 0x0D4    | RO     |
| HMAC_RD_RESULT_6_REG         | Hash result register 6                                                                      | 0x0D8    | RO     |
| HMAC_RD_RESULT_7_REG         | Hash result register 7                                                                      | 0x0DC    | RO     |

**Configuration Register**

- HMAC_SET_MESSAGE_PAD_REG   | Software padding register                                                                   | 0x0FO    | WO     |
- HMAC_ONE_BLOCK_REG          | One block message register                                                                  | 0x0F4    | WO     |
- HMAC_SOFT_JTAG_CTRL_REG    | Re-enable JTAG register 0                                                                  | 0x0F8    | WO     |
- HMAC_WR_JTAG_REG            | Re-enable JTAG register 1                                                                  | 0x0FC    | WO     |

**Version Register**

| Name                          | Description                                                                                   | Address   | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|----------|--------|
| HMAC_DATE_REG                | Version control register                                                                       | 0x1FC    | R/W    |

---

*Espressif Systems*

Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)