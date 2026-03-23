

```markdown
Register 34.50. SLCHOST_SLCOHOST_TOKEN_RDATA_REG (0x0044)

| 31 | 28 | 27 | 16 | 15 |
|----:|----:|----:|----:|----:|
| OxO |     |     | OxO | Reset |

SLCHOST_HOSTSLCHOST_SLCO_TOKEN1 Represents the SLCO accumulated number of buffers for receiving data. (RO)

Register 34.51. SLCHOST_PKT_LEN_REG (0x0060)

| 31 | 20 | 19 | 0 |
|----:|----:|----:|---|
| OxO |     |     | Reset |

SLCHOST_HOSTSLCHOST_SLCO_LEN Represents the accumulated length of data that the slave wants to send. The value gets updated only when the host reads it. (RO)

SLCHOST_HOSTSLCHOST_SLCO_LEN_CHECK Check SLCHOST_HOSTSLCHOST_SLCO_LEN. Its value is SLCHOST_HOSTSLCHOST_SLCO_LEN bit[9:0] plus bit[19:10]. (RO)
```