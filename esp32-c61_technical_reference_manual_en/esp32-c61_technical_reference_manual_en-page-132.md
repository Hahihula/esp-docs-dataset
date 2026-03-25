

```markdown
| Field name     | Bit Width | Description                                                                 |
|----------------|-----------|-----------------------------------------------------------------------------|
| format         | 2         | 11 (sync): Synchronization                                                  |
| subformat      | 2         | 01 (exception): Exception cause and trap handler address                    |
| branch         | 1         | Set to 0 if the address points to a branch instruction, and the branch was taken. Set to 1 if the instruction is not a branch or if the branch is not taken. |
| privilege      | 1         | The privilege level of the reported instruction                             |
| ecause         | 6         | Exception cause                                                             |
| interrupt      | 1         | Interrupt                                                                   |

| Field name     | Bit Width | Description                                                                 |
|----------------|-----------|-----------------------------------------------------------------------------|
| theaddr        | 1         | When set to 1, the address field points to the trap handler address. When set to 0, the address field points to the EPC (exception program counter) for an exception at the target for an updiscon, and is undefined for other exceptions and interrupts. |
| address        | 31        | Full instruction address. The value of this field must be left shifted 1 bit in order to recreate the original byte address. |
| tvalepc        | 32        | Value from appropriate utval/stval/mtval CSR (control/status register). Omitted if the interrupt is 1 |
| sign_extend    | 3         | Reserved                                                                     |

## Format 3 Subformat 3 - Support

This packet provides supporting information to aid the decoder. It is issued when the trace is ended, filter match is failed, or a packet is lost. The length is 2 bytes.

Table 2.6-5. Packet format 3 subformat 3
```