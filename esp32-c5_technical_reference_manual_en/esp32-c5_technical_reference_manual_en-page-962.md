

```markdown
Register 28.6. ECDSA_INT_ENA_REG (0x0014)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3   | ECDSA_SHA_RELEASE_INT_ENA     Write 1 to enable the ECDSA_SHA_RELEASE_INT interrupt. (R/W) |
| 2   | ECDSA_POST_DONE_INT_ENA       Write 1 to enable the ECDSA_POST_DONE_INT interrupt. (R/W) |
| 1   | ECDSA_PROC_DONE_INT_ENA       Write 1 to enable the ECDSA_PROC_DONE_INT interrupt. (R/W) |
| 0   | ECDSA_PREP_DONE_INT_ENA       Write 1 to enable the ECDSA_PREP_DONE_INT interrupt. (R/W) |

Register 28.7. ECDSA_INT_CLR_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3   | ECDSA_SHA_RELEASE_INT_CLR     Write 1 to clear the ECDSA_SHA_RELEASE_INT interrupt. (WT) |
| 2   | ECDSA_POST_DONE_INT_CLR       Write 1 to clear the ECDSA_POST_DONE_INT interrupt. (WT) |
| 1   | ECDSA_PROC_DONE_INT_CLR       Write 1 to clear the ECDSA_PROC_DONE_INT interrupt. (WT) |
| 0   | ECDSA_PREP_DONE_INT_CLR       Write 1 to clear the ECDSA_PREP_DONE_INT interrupt. (WT) |
```