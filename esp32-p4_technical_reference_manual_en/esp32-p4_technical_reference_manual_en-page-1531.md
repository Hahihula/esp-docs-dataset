

```markdown
Register 31.5. ECDSA_INT_ST_REG (0x0010)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 4   | 3                                       | 2                                                                               | 1                                                                               | 0                                                                               |
|     |                                         | Reset                                                                          |

ECDSA_PREP_DONE_INT_ST The masked interrupt status of the ECDSA_PREP_DONE_INT interrupt. (RO)

ECDSA_PROC_DONE_INT_ST The masked interrupt status of the ECDSA_PROC_DONE_INT interrupt. (RO)

ECDSA_POST_DONE_INT_ST The masked interrupt status of the ECDSA_POST_DONE_INT interrupt. (RO)

ECDSA_SHA_RELEASE_INT_ST The masked interrupt status of the ECDSA_SHA_RELEASE_INT interrupt. (RO)


Register 31.6. ECDSA_INT_ENA_REG (0x0014)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 4   | 3                                       | 2                                                                               | 1                                                                               | 0                                                                               |
|     |                                         | Reset                                                                          |

ECDSA_PREP_DONE_INT_ENA Write 1 to enable the ECDSA_PREP_DONE_INT interrupt. (R/W)

ECDSA_PROC_DONE_INT_ENA Write 1 to enable the ECDSA_PROC_DONE_INT interrupt. (R/W)

ECDSA_POST_DONE_INT_ENA Write 1 to enable the ECDSA_POST_DONE_INT interrupt. (R/W)

ECDSA_SHA_RELEASE_INT_ENA Write 1 to enable the ECDSA_SHA_RELEASE_INT interrupt. (R/W)
```