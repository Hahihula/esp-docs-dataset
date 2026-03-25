

```markdown
Register 22.10. RSA_QUERY_CLEAN_REG (0x0808)

31 | [reserved] | RSA_QUERY_CLEAN
----------------------------------------------------------------------------------------------------
0   |            | Reset

RSA_QUERY_CLEAN Represents whether or not the RSA memory completes initialization.
O: Not complete
1: Completed
(RO)


Register 22.11. RSA_INT_CLR_REG (0x081C)

31 | [reserved] | RSA_CLEAR_INTERRUPT
----------------------------------------------------------------------------------------------------
0   |            | Reset

RSA_CLEAR_INTERRUPT Write 1 to clear the RSA interrupt. (WT)


Register 22.12. RSA_INT_ENA_REG (0x082C)

31 | [reserved] | RSA_INT_ENA
----------------------------------------------------------------------------------------------------
0   |            | Reset

RSA_INT_ENA Write 1 to enable the RSA interrupt. (R/W)


Register 22.13. RSA_DATE_REG (0x0830)

31 30 29 | [reserved] | RSA_DATE
----------------------------------------------------------------------------------------------------
0   0    |            | Reset

RSA_DATE Version control register. (R/W)
```