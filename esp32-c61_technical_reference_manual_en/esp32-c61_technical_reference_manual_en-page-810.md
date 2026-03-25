

```markdown
Register 22.6. ECDSA_INT_ENA_REG (0x0014)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3-0 | Reset: 0000                                                                |

ECDSA_PREP_DONE_INT_ENA Write 1 to enable the ECDSA_PREP_DONE_INT interrupt. (R/W)
ECDSA_PROC_DONE_INT_ENA Write 1 to enable the ECDSA_PROC_DONE_INT interrupt. (R/W)
ECDSA_POST_DONE_INT_ENA Write 1 to enable the ECDSA_POST_DONE_INT interrupt. (R/W)
ECDSA_SHA_RELEASE_INT_ENA Write 1 to enable the ECDSA_SHA_RELEASE_INT interrupt. (R/W)

Register 22.7. ECDSA_INT_CLR_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3-0 | Reset: 0000                                                                |

ECDSA_PREP_DONE_INT_CLR Write 1 to clear the ECDSA_PREP_DONE_INT interrupt. (WT)
ECDSA_PROC_DONE_INT_CLR Write 1 to clear the ECDSA_PROC_DONE_INT interrupt. (WT)
ECDSA_POST_DONE_INT_CLR Write 1 to clear the ECDSA_POST_DONE_INT interrupt. (WT)
ECDSA_SHA_RELEASE_INT_CLR Write 1 to clear the ECDSA_SHA_RELEASE_INT interrupt. (WT)
```