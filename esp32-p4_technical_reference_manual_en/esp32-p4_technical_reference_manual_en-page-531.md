

```markdown
Register 8.41. EFUSE_INT_ST_REG (0x01DC)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 2   | `EFUSE_PGM_DONE_INT_ST` The masked interrupt status of EFUSE_PGM_DONE_INT. (RO) |
| 1   | `EFUSE_READ_DONE_INT_ST` The masked interrupt status of EFUSE_READ_DONE_INT. (RO) |
| 0   | Reset |

```markdown
Register 8.42. EFUSE_INT_ENA_REG (0x01E0)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 2   | `EFUSE_PGM_DONE_INT_ENA` Write 1 to enable EFUSE_PGM_DONE_INT. (R/W) |
| 1   | `EFUSE_READ_DONE_INT_ENA` Write 1 to enable EFUSE_READ_DONE_INT. (R/W) |
| 0   | Reset |

```markdown
Register 8.43. EFUSE_INT_CLR_REG (0x01E4)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 2   | `EFUSE_PGM_DONE_INT_CLR` Write 1 to clear EFUSE_PGM_DONE_INT. (WT) |
| 1   | `EFUSE_READ_DONE_INT_CLR` Write 1 to clear EFUSE_READ_DONE_INT. (WT) |
| 0   | Reset |
```