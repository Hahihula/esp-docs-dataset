

```markdown
Register 25.6. ECDSA_INT_ENA_REG (0x0014)

ECDSA_CALC_DONE_INT_ENA Write 1 to enable the ECDSA_CALC_DONE_INT interrupt. (R/W)
ECDSA_SHA_RELEASE_INT_ENA Write 1 to enable the ECDSA_SHA_RELEASE_INT interrupt. (R/W)

Register 25.7. ECDSA_INT_CLR_REG (0x0018)

ECDSA_CALC_DONE_INT_CLR Write 1 to clear the ECDSA_CALC_DONE_INT interrupt. (WT)
ECDSA_SHA_RELEASE_INT_CLR Write 1 to clear the ECDSA_SHA_RELEASE_INT interrupt. (WT)

Register 25.8. ECDSA_STATE_REG (0x0020)

ECDSA_BUSY Represents the working status of the ECDSA accelerator.
0: IDLE
1: LOAD
2: GET
3: BUSY
(RO)
```