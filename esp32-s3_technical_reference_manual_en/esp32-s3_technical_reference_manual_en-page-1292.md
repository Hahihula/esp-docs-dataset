**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Navigation Link:**
GoBack

**Continuation Notice:**
Continued from the previous page ...

**Register Description and Values for Register 34.11, SDHOST_CMD_REG (0x002C):**

- **SDHOST_TRANSFER_MODE:** 
  - Value: `0`
  - Description: Block data transfer command; 1: Stream data transfer command.
  - Access Rights: Read/Write

- **SDHOST_READ_WRITE**
  - Value: `0`
  - Description: Read from card; 1: Write to card. Don’t care if no data is expected from card.

- **SDHOST_DATA_EXPECTED**
  - Value: `0`
  - Description: No data transfer expected; 1: Data transfer expected.
  - Access Rights: Read/Write

- **SDHOST_CHECK_RESPONSE_CRC**
  - Value: `0`
  - Description: Do not check; 1: Check response CRC. Some of command responses do not return valid CRC bits. Software should disable CRC checks for those commands in order to disable CRC checking by controller.
  - Access Rights: Read/Write

- **SDHOST_RESPONSE_LENGTH**
  - Value: `0`
  - Description: Short response expected from card; 1: Long response expected from card.

- **SDHOST_RESPONSE_EXPECTED**
  - Value: `0`
  - Description: No response expected from card; 1: Response expected from card.
  - Access Rights: Read/Write

- **SDHOST_CMD_INDEX**
  - Description: Command index. (R/W)

**Register Descriptions for Other Registers Mentioned in the Document:**

- **Register 34.12, SDHOST_RESP0_REG (0x0030):**
  - Description:
    ```
    31
     0
     0x00000000 Reset
    ```

- **Register 34.13, SDHOST_RESP1_REG (0x0034):**
  - Description:
    ```
    31
     0
     0x00000000 Reset
    ```

- **Register 34.14, SDHOST_RESP2_REG (0x0038):**
  - Description:
    ```
    31
     0
     0x00000000 Reset
    ```

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)