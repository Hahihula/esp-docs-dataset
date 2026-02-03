Title: Chapter 27 I2C Controller (I2C)

Subtitle: GoBack

Section Title: 27.5.1 Introduction

### Figure Caption:
- **Figure 27.5-1**: I2Cmaster Writing to I2Cslave with a 7-bit Address

#### Diagram Description:
The diagram shows the communication between an "I2Cmaster" and an "I2Cslave". The master sends commands via SCL (Serial Clock Line) and data through SDA (Serial Data Line). It includes fields for `cmd`, `op_code`, `byte_num` on the Master side, with corresponding RAM addresses (`addr0`, `addr1`, etc.) being written to by the slave. On the Slave side, there are similar fields but labeled as "Slave addr<<1| r/w" indicating read/write operations.

#### Text Content:
- **Body Text**:
  - Figure caption: Shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit addressing.
  - Description explains the process, including writing a R/W bit for write operation and storing remaining bits in the command box.

#### Steps Listed Under "Configuration Example":
1. Configure timing parameters according to Section [27.4.7](#).
2. Set `I2C_MS_MODE` (master) to 1.
3. Write synchronization commands: `I2C_CONF_UPGATE` and `I2C_CONF_UPGRADE`.
4. Configure command registers of I2Cmaster.

#### Table:
- **Table Title**: Command register

| Command register | op_code | ack_value | ack_exp | ack_check_err | byte_num |
|------------------|---------|----------|--------|---------------|----------|
| `I2C_COMMAND`    | RSTART  | —       | —     |               |          |
| `I2C_COMMAND1`   | WRITE   | ack_value | ack_exp | N+1           |          |

#### Footer:
- **Text**: Espressif Systems
- **Page Number and Document Version**: ESP32-S3 TRM (Version 1.7)
- **Link Texts**: Submit Documentation Feedback

(Note: The text content is transcribed as it appears in the image, including any potential typographical errors or inconsistencies.)