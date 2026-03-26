

```markdown
Register 30.7. DSA_QUERY_CHECK_REG (0xOE14)

DSA_PADDING_BAD Represents whether the padding check passes.
O: The padding check passes.
1: The padding check fails.
(RO)

DSA_MD_ERROR Represents whether the MD check passes.
O: The MD check passes.
1: The MD check fails.
(RO)


Register 30.8. DSA_KEY_SOURCE_REG (0xOE18)

DSA_KEY_SOURCE Represents the source of RSA_DS_KEY.
O: HMAC
1: Key Manager
(R/W)


Register 30.9. DSA_DATE_REG (0xOE20)

DSA_DATE Version control register. (R/W)
```