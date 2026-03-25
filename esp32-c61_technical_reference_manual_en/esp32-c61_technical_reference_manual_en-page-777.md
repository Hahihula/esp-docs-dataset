

```markdown
will be cleared.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 9 Interrupt Matrix > Section 9.2 Interrupt Terminology in ESP32-C61.
```

## 20.7 Programming Procedures

The programming procedure for configuring ECC is described below:

1. Configure the ECC clock and reset. Refer to Section 20.5 for detailed information.

2. Select the key size and working mode as described in Section 20.4.

3. Enable the `ECC_MULT_CALC_DONE_INT` interrupt as described in Section 20.6.

4. Set the `ECC_MULT_START` field to start ECC calculation.

5. Wait for the `ECC_MULT_CALC_DONE_INT` interrupt, which indicates the completion of the ECC calculation.

6. Check the result as described in Section 20.4.
```