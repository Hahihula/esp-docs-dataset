**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Register Information:**
- Register Name: IDSTS_REG (0x008C)
- Bit Positions and Values:
  - [31] (reserved)
  - [16, 15, ..., 9, ..., 4, ..., 2, ..., 1]
    - IDsFS_FSM
    - IDsFS_FBE_CODE
    - IDsFS_AIS
    - IDsFS_NIS
    - IDsFS_CES
    - IDsFS_DU
    - IDsFS_FBE
    - IDsFS_RI
    - IDsFS_TI

**Bit Descriptions:**

- **IDSTS_FSM**
  - DMAC FSM present state (RO)
  - Values:
    - `0`: DMA_IDLE
    - `1`: DMA_SUSPEND
    - `2`: DESC_RD
    - `3`: DESC_CHK
    - `4`: DMA_RD_REQ_WAIT
    - `5`: DMA_WR_REQ_WAIT
    - `6`: DMA_RID
    - `7`: DMA_WR
    - `8`: DESC_CLOSE

- **IDSTS_FBE_CODE**
  - Fatal Bus Error Code. Indicates the type of error that caused a Bus Error.
  - Valid only when the Fatal Bus Error bit IDs[2] is set.

- **3b001: Host Abort received during transmission**

- **3b010: Host Abort received during reception**

- **Others:** Reserved

- **IDSTS_AIS**
  - Abnormal Interrupt Summary. Logical OR of:
    - `IDSFS_FBE_CODE`: Fatal Bus Interrupt
    - `IDSFS_CES`: Card Error Summary (RO)
  - Description for each bit:

- **IDSTS_NIS**
  - Normal Interrupt Summary.
  - Logical OR: 
    - `IDSFS_FBE_CODE`: Transmit Interrupt

- **IDSTS_CES**
  - Card Error Summary. Indicates the status of transactions to/from card, also present in RINTSTS.

- **IDSTS_DU**
  - Descriptor Unavailable Interrupt
  - Description:
    - When bit = 0 (DESO[31] = 0), writing clears this bit.
  
- **IDSTS_FBE**
  - Fatal Bus Error Interrupt. Indicates that a bus error occurred when the bit is set, DMA disables all its access.

- **IDSTS_RI**
  - Receive Interrupt
  - Description: Indicates completion of data reception for descriptor

- **IDSTS_TI**
  - Transmit Interrupt.
  - Description: Indicates finished data transmission for descriptor
  
**Footer Information:** 
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)