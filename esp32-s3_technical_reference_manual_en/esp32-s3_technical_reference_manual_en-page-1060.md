**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** GoBack

**Table of TX status registers:**

| Name                | Description                                    | I2S0 Address       | I2S1 Address       | Access |
|---------------------|-------------------------------------------------|--------------------|--------------------|--------|
| **TX status registers** |                                              |                    |                    |        |
| `I2S_STATE_REG`    | TX status register                              | 0x006C             | 0x006C             | RO     |
| `Version register`  | Version control register                        | 0x0080             | 0x0080             | R/W    |
| `I2S_DATE_REG`     |                                              |                    |                    |        |

**Section Title:**
28.14 Registers

**Subsection with Register Description and Address Information (Register 28.1):**

- **Register Name:** I2S_INT_RAW_REG
- **Address:** 0x000C
  
  - `I2S_RX_DONE_INT_RAW`: The raw interrupt status bit for I2S_RXDoneInt interrupt.
  
    Access: RO/WTC/SS

  - `I2S_TX_DONE_INT_RAW`: The raw interrupt status bit for I2STxDoneInt interrupt.

    Access: RO/WTC/SS
  
  - `I2S_RX_HUNG_INT_RAW`: The raw interrupt status bit for I2S_RxHungInt interrupt.
  
    Access: (RO/WTC/SS)
  
  - `I2S_TX_HUNG_INT_RAW`: The raw interrupt status bit for I2STxHungInt interrupt.

    Access: RO/WTC/SS

**Subsection with Register Description and Address Information (Register 28.2):**

- **Register Name:** I2S_INT_ST_REG
- **Address:** 0x0010
  
  - `I2S_RX_DONE_INT_ST`: The masked interrupt status bit for I2S_RXDoneInt interrupt.
  
    Access: RO
  
  - `I2S_TX_DONE_INT_ST`: The masked interrupt status bit for I2STxDoneInt interrupt.

    Access: (RO)
  
  - `I2S_RX_HUNG_INT_ST`: The masked interrupt status bit for I2S_RxHungInt interrupt.
  
    Access: RO
  
  - `I2S_TX_HUNG_INT_ST`: The masked interrupt status bit for I2STxHungInt interrupt.

    Access: (RO)

**Footer Information:** 
Espressif Systems
1060 Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)