

```markdown
| Field name   | Bits | Description                  |
|--------------|------|------------------------------|
| sign_extend  | 3    | Reserved                     |

## Format 3 Subformat 1 - Exception

This packet also contains all the information the decoder needs to fully identify an instruction. It is sent following an exception or interrupt, and includes the cause, the 'trap value' (for exceptions), and the address of the trap handler or of the exception itself. The length is 10 bytes.

Table 2.6-4. Packet format 3 subformat 1

| Field name   | Bits | Description                                                                                      |
|--------------|------|--------------------------------------------------------------------------------------------------|
| format       | 2    | 11 (sync): Synchronization                                                                       |
| subformat    | 2    | 01 (exception): Exception cause and trap handler address                                         |
| branch       | 1    | Set to 0 if the address points to a branch instruction, and the branch was taken. Set to 1 if the instruction is not a branch or if the branch is not taken. |
| privilege    | 1    | The privilege level of the reported instruction                                                 |
| ecause       | 5    | Exception cause                                                                                 |
| interrupt    | 1    | Interrupt                                                                                       |
| address      | 31   | Full instruction address. The value of this field must be left shifted 1 bit in order to recreate original byte address. |
| tvalepc      | 32   | Exception address if ecause is 2 and interrupt is 0, or trap value otherwise                    |
| sign_extend  | 6    | Reserved                                                                                        |

## Format 3 Subformat 3 - Support

This packet provides supporting information to aid the decoder. It is issued when the trace is ended. The length is 1 byte.

Table 2.6-5. Packet format 3 subformat 3

| Field name   | Bits | Description                                                                                                                                                                                                 |
|--------------|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format       | 2    | 11 (sync): Synchronization                                                                                                                                                                                   |
| subformat    | 2    | 11 (support): Supporting information for the decoder                                                                                                                                                         |
| enable       | 1    | Indicates if the encoder is enabled                                                                                                                                                                           |
| qual_status  | 2    | Indicates qualification status:<br>• 00 (no_change): No change to filter qualification<br>• 01 (ended_rep): Qualification ended, preceding instruction sent explicitly to indicate last qualification instruction<br>• 10 (trace lost): One or more packets lost<br>• 11 (ended_upd): Qualification ended, preceding te_inst would have been sent anyway due to an updicon, even if wasn't the last qualified instruction |
| sign_extend  | 1    | Reserved                                                                                                                                                                                                   |
```