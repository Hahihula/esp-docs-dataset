

```markdown
| Field name   | Bits | Description                                                                 |
|--------------|------|-----------------------------------------------------------------------------|
| format       | 2    | 11 (sync): Synchronization                                                  |
| subformat    | 2    | 01 (exception): Exception cause and trap handler address                    |
| branch       | 1    | Set to 0 if the address points to a branch instruction, and the branch was taken. Set to 1 if the instruction is not a branch or if the branch is not taken. |
| privilege     | 1    | The privilege level of the reported instruction                             |
| ecause       | 6    | Exception cause                                                             |
| interrupt     | 1    | Interrupt                                                                  |

When set to 1, the address field points to the trap handler address. When set to 0, the address field points to the EPC (exception program counter) for an exception at the target for an updiscon, and is undefined for other exceptions and interrupts.

| theaddr       | 1    |                                                                             |
|---------------|------|-----------------------------------------------------------------------------|
| address       | 31   | Full instruction address. The value of this field must be left shifted 1 bit in order to recreate the original byte address. |
| tvalepc       | 32   | Value from appropriate utval/stval/mtval CSR (control/status register). Omitted if the interrupt is 1 |
| sign_extend   | 3    | Reserved                                                                    |

## Format 3 Subformat 3 - Support

This packet provides supporting information to aid the decoder. It is issued when the trace is ended, filter match is failed, or a packet is lost. The length is 2 bytes.

```markdown
| Field name     | Bits | Description                                                                 |
|----------------|------|-----------------------------------------------------------------------------|
| format         | 2    | 11 (sync): Synchronization                                                  |
| subformat      | 2    | 11 (support): Supporting information for the decoder                         |
| enable         | 1    | Indicates if the encoder is enabled                                        |
| encoder_mode   | 1    | Always 0. Only supported by branch trace                                    |

Indicates qualification status:
- 00 (no_change): No change to filter qualification
- 01 (ended_rep): Qualification ended, preceding instruction sent explicitly to indicate last qualification instruction
- 10 (trace lost): One or more packets lost
- 11 (ended_upd): Qualification ended, preceding te_inst would have been sent anyway due to an updiscon, even if wasn't the last qualified instruction

| qual_status   | 2    |
```