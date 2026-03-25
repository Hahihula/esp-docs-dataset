

```markdown
## 34.4.3.5 Error Passive Interrupt (EPI)

The Error Passive Interrupt (EPI) is triggered whenever the TWAI controller switches from Error Active to Error Passive, or vice versa.

## 34.4.3.6 Arbitration Lost Interrupt (ALI)

The Arbitration Lost Interrupt (ALI) is triggered whenever the TWAI controller is attempting to transmit a message and loses arbitration. The bit position where the TWAI controller lost arbitration is automatically recorded in the Arbitration Lost Capture register (`TWAI_ARB_LOST_CAP_REG`). When the ALI occurs again, the Arbitration Lost Capture register will no longer record a new bit location until it is cleared (via CPU reading this register).

## 34.4.3.7 Bus Error Interrupt (BEI)

The Bus Error Interrupt (BEI) is triggered whenever the TWAI controller detects an error on the TWAI bus. When a bus error occurs, the Bus Error type and its bit position are automatically recorded in the Error Code Capture register (`TWAI_ERR_CODE_CAP_REG`). When the BEI occurs again, the Error Code Capture register will no longer record new error information until it is cleared (via a read from the CPU).

## 34.4.3.8 Bus Idle Status Interrupt (BISI)

The Bus Idle Status Interrupt (BISI) is triggered when the number of clock cycles of the TWAI controller in the idle status exceeds the pre-configured value in the `TWAI_IDLE_INTR_CNT_REG` register. Users can configure this interrupt to get the TWAI controller idle status and further decide whether to turn off the external TWAI receiver to reduce the overall power consumption (see Section 34.4.10).

## 34.4.4 Transmit and Receive Buffers

### 34.4.4.1 Overview of Buffers

Table 34.4-3. Buffer Layout for Standard Frame Format and Extended Frame Format

| Standard Frame Format (SFF) |  | Extended Frame Format (EFF) |  |
| Offset Address | Content | Offset Address | Content |
|------------------|------------------------------------------|------------------|------------------------------------------|
| 0x40             | TX/RX frame information                  | 0x40             | TX/RX frame information                  |
| 0x44             | TX/RX identifier 1                       | 0x44             | TX/RX identifier 1                       |
| 0x48             | TX/RX identifier 2                       | 0x48             | TX/RX identifier 2                       |
| 0x4c             | TX/RX data byte 1                        | 0x4c             | TX/RX identifier 3                       |
| 0x50             | TX/RX data byte 2                        | 0x50             | TX/RX identifier 4                       |
| 0x54             | TX/RX data byte 3                        | 0x54             | TX/RX data byte 1                        |
| 0x58             | TX/RX data byte 4                        | 0x58             | TX/RX data byte 2                        |
| 0x5c             | TX/RX data byte 5                        | 0x5c             | TX/RX data byte 3                        |
| 0x60             | TX/RX data byte 6                        | 0x60             | TX/RX data byte 4                        |

Cont'd on next page
```