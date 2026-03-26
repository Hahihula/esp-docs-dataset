

```markdown
Register 31.7. ECDSA_INT_CLR_REG (0x0018)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 4   | ECDsA_SHA_RELEASE_INT_CLR   | Write 1 to clear the ECDSA_SHA_RELEASE_INT interrupt. (WT)                   |
| 3   | ECDsA_POST_DONE_INT_CLR     | Write 1 to clear the ECDSA_POST_DONE_INT interrupt. (WT)                     |
| 2   | ECDsA_PROC_DONE_INT_CLR     | Write 1 to clear the ECDSA_PROC_DONE_INT interrupt. (WT)                     |
| 1   | ECDsA_PREP_DONE_INT_CLR     | Write 1 to clear the ECDSA_PREP_DONE_INT interrupt. (WT)                     |
| 0   |                             | Reset                                                                       |

ECDSA_PREP_DONE_INT_CLR    Write 1 to clear the ECDSA_PREP_DONE_INT interrupt. (WT)
ECDSA_PROC_DONE_INT_CLR    Write 1 to clear the ECDSA_PROC_DONE_INT interrupt. (WT)
ECDSA_POST_DONE_INT_CLR    Write 1 to clear the ECDSA_POST_DONE_INT interrupt. (WT)
ECDSA_SHA_RELEASE_INT_CLR  Write 1 to clear the ECDSA_SHA_RELEASE_INT interrupt. (WT)

Register 31.8. ECDSA_STATE_REG (0x0020)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 2   | ECDsA_BUSY                   | Represents the working state of the ECDSA_DS module.                         |
| 1   |                             | Reset                                                                       |

ECDSA_BUSY                  Represents the working state of the ECDSA_DS module.
0: IDLE
1: LOAD
2: Reserved
3: BUSY
(RO)
```