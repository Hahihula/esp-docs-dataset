
```markdown
| Field name     | Bits   | Description                                                                                                                                                                                                 |
|----------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| branch_map     | Variable| An array of bits indicating whether branches are taken or not. Bit 0 represents the oldest branch instruction executed. For each bit:<ul><li>0: branch taken</li><li>1: branch not taken</li></ul>The field Bits is variable and determined by the branches field. |
| notify         | 1      | If the value of this bit is different from the MSB of address, it indicates that this packet is reporting an instruction that is not the target of an uninferable discontinuity because a notification was requested via trigger[2] or a filter matched.                                                                 |
| updiscon       | 1      | If the value of this bit is different from notify, it indicates that this packet is reporting the instruction following an uninferable discontinuity and is also the instruction before an exception, privilege change or resync.                                                         |
| zero_ext       | Variable| The length of this field is determined by branches as follows:<ul><li>1: 6 bits</li><li>2 ~ 3: 4 bits</li><li>4 ~ 31: 0 bits</li></ul>                                                                                   |
| address        | Variable| Delta instruction address. These bits can be 8/16/24/32                                                                                                                                                     |

Format 1 - no address, branch_map

The length is 5 bytes.

Table 2.6-8. Packet format 1 without address
```