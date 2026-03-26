

```markdown
| Field name   | Bits | Description                                                                 |
|--------------|------|-----------------------------------------------------------------------------|
| zero_extend  | 4    | Reserved                                                                    |
| address      | Variable | Delta instruction address. These bits can be 8/16/24/32.                  |

### 2.6.3.3 Format 1 Packets

This packet includes branch information, and is used when either the branch information must be reported (for example because the branch map is full), or when the address of instruction must be reported, and there has been at least one branch since the previous packet.

The packet length is variable if delta address mode is enabled, ranging from 5 bytes to 12 bytes. The address field can be 8/16/24/32 bits, inferred from the packet length. For example:

- The header length is *n* bytes
- The value of the format field is 1
- The value of the branch field is:
    - 0: the packet is format 1 without address
    - 1: branch_map is 1 bit wide, zero_ext is 6 bits wide, and address is *n* − 5 bits wide
    - 2 ~ 3: branch_map is 3 bits wide, zero_ext is 4 bits wide, and address is *n* − 5 bits wide
    - 4 ~ 7: branch_map is 7 bits wide, zero_ext is 0 bits wide, and address is *n* − 5 bits wide
    - 8 ~ 15: branch_map is 15 bits wide, zero_ext is 0 bits wide, and address is *n* − 6 bits wide
    - 16 ~ 31: branch_map is 31 bits wide, zero_ext is 0 bits wide, and address is *n* − 8 bits wide

#### Format 1 - address, branch_map

The length is variable.

Table 2.6-7. Packet format 1 with address

| Field name | Bits | Description                                                                 |
|------------|------|-----------------------------------------------------------------------------|
| format     | 2    | 01: Includes branch information                                             |
| branches   | 5    | Number of valid bits branch_map. The number of bits of branch_map is determined as follows:<ul><li>0: (cannot occur for this format)</li><li>1: 1 bit</li><li>2 ~ 3: 3 bits</li><li>4 ~ 7: 7 bits</li><li>8 ~ 15: 15 bits</li><li>16 ~ 31: 31 bits</li></ul>For example if branches = 12, branch_map is 15-bit long, and the 12 LSBs are valid. |
```