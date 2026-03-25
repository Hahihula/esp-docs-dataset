

```markdown
| Field name | Bits | Description |
|:-----------|:------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format     | 2     | 10 (addr-only): No branch information                                                                                                                                                    |
| address    | 31    | Full instruction address                                                                                                                                                              |
| notify     | 1     | ESP32-H2 don't support notification, so this bit is always same with the MSB of address.                                                                                             |
| updiscon   | 1     | If the value of this bit is different from notify, it indicates that this packet is reporting the instruction following an unifiable discontinuity and is also the instruction before an exception, privilege change or resync. |
| sign_extend| 5     ||

**Table 2.6-6. Packet format 2**

## 2.6.3.3 Format 1 Packets

This packet includes branch information, and is used when either the branch information must be reported (for example because the branch map is full), or when the address of instruction must be reported, and there has must been at least one branch since the previous packet. This packet only supports full address mode.

**Format 1- address, branch_map**

The length is variable.

```markdown
| Field name | Bits | Description |
|:-----------|:------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format     | 2     | 01: Includes branch information<br>Number of valid bits in branch_map. The number of bits of branch_map is determined as follows:<ul><li>0: (cannot occur for this format)</li><li>1: 1 bit</li><li>2-3: 3 bits</li><li>4-7: 7 bits</li><li>8-15: 15 bits</li><li>16-31: 31 bits</li></ul>For example if branches = 12, branch_map is 15-bit long, and the 12 LSBs are valid. |
| branches   | 5     ||

branch_map | Variable | An array of bits indicating whether branches are taken or not. Bit 0 represents the oldest branch instruction executed. For each bit:<ul><li>0: branch taken</li><li>1: branch not taken</li></ul>The field bits is variable and determined by the "branches" field. |
| address    | 31    | Full instruction address                                                                                                                                                              |
| notify     | 1     | ESP32-H2 don't support notification, so this bit is always same with the MSB of address.                                                                                             |
| updiscon   | 1     | If the value of this bit is different from notify, it indicates that this packet is reporting the instruction following an unifiable discontinuity and is also the instruction before an exception, privilege change or resync. |

**Table 2.6-7. Packet format 1 with address**
```