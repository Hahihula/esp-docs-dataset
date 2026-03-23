

```markdown
Chapter 24 Digital Signature (DS)

10. Read the signed result: Read the signed result Zᵢ (i ∈ {0, 1, ..., n−1}), where n = N/32, from memory block DS_Z_MEM. The memory block stores Z in little-endian byte order.

11. Exit the operation: Write 1 to DS_SET_FINISH_REG, and then poll DS_QUERY_BUSY_REG until the software reads 0.
```