

```markdown
## Table 2.6-1. Header Format

| Field       | Bits | Description          | Value   |
|-------------|------|----------------------|---------|
| length      | 5    | Length of whole packet | 4~13    |
| placeholder | 3    | Reserved             | 0       |

## Table 2.6-2. Index Format

| Field   | Bits | Description          | Value     |
|---------|------|----------------------|-----------|
| index   | 16   | The index of each packet | 0~65536  |

## Table 2.6-3. Packet format 3 subformat 0

| Field name | Bits | Description                                                                                       |
|------------|------|---------------------------------------------------------------------------------------------------|
| format     | 2    | 11 (sync): Synchronization                                                                       |
| subformat  | 2    | 00 (start): Start of tracing, or resync                                                          |
| branch     | 1    | Set to 0 if the address points to a branch instruction, and the branch was taken. Set to 1 if the instruction is not a branch or if the branch is not taken. |
| privilege  | 1    | The privilege level of the reported instruction                                                  |
| address    | 31   | Full instruction address. The address must be left shifted 1 bit in order to recreate the original byte address. |
```