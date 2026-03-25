

```markdown
| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
|               | 0x1A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x2A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x5A     | 1-bit mode  | 2-bit mode | -          |
|               | 0xAA     | 1-bit mode  | 4-bit mode | -          |
| End_SEG_TRANS | 0x05     | 1-bit mode  | -          | -          |
| En_QPI         | 0x06     | 1-bit mode  | -          | -          |

Table 33.5-14. CMD Values Supported in QPI Mode
```