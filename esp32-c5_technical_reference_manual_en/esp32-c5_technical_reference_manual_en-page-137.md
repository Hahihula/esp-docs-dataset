

```markdown
Table 3.6-1. Header Format

| Field      | Bit Width | Description                  | Value   |
|------------|-----------|------------------------------|---------|
| length     | 5         | Length of whole packet       | 4 ~ 13  |
| flow       | 2         | Reserved                     | 0       |
| timestamp  | 1         | Reserved                     | 0       |

## 3.6.2 Index

Index has 2 bytes. The format of index is shown in Table 3.6-2.

Table 3.6-2. Index Format

| Field   | Bit Width | Description                  | Value     |
|---------|-----------|------------------------------|-----------|
| index   | 16        | The index of each packet     | 0~65536   |

## 3.6.3 Payload

The length of payload ranges from 1 byte to 10 bytes.

### 3.6.3.1 Format 3 Packets

Format 3 packets are used for synchronization, and report supporting information. There are 4 subformats defined in the specification. ESP32-C5 only supports 3 of them.

#### Format 3 Subformat 0 - Synchronization

This packet contains all the information the decoder needs to fully identify an instruction. It is sent for the first traced instruction (unless that instruction also happens to be the first one in an exception handler), and when synchronization has been scheduled by the expiry of the synchronization timer. The payload length is 5 bytes.

Table 3.6-3. Packet format 3 subformat 0

| Field name | Bit Width | Description                                                                 |
|------------|-----------|-----------------------------------------------------------------------------|
| format     | 2         | 11 (sync): Synchronization                                                  |
| subformat  | 2         | 00 (start): Start of tracing, or resync                                     |
| branch     | 1         | Set to 0 if the address points to a branch instruction, and the branch was taken. Set to 1 if the instruction is not a branch or if the branch is not taken. |
| privilege  | 1         | The privilege level of the reported instruction                             |
| address    | 31        | Full instruction address. The address must be left shifted 1 bit in order to recreate the original byte address. |
| sign_extend| 3         | Reserved                                                                    |

#### Format 3 Subformat 1 - Exception

This packet also contains all the information the decoder needs to fully identify an instruction. It is sent following an exception or interrupt, and includes the cause, the 'trap value' (for exceptions), and the address
```