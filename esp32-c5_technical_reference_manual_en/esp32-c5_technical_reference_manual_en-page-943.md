

```markdown
## Register 27.6. DS_QUERY_CHECK_REG (0xOE14)

DS_PADDING_BAD
DS_MD_ERROR

DS_MD_ERROR Represents whether or not the MD check passes.
O: The MD check passes
1: The MD check fails
(RO)

DS_PADDING_BAD Represents whether or not the padding check passes.
O: The padding check passes
1: The padding check fails
(RO)

## Register 27.7. DS_KEY_SOURCE_REG (0xOE18)

DS_KEY_SOURCE

DS_KEY_SOURCE Represents the source of the DSA_KEY.
O: HMAC
1: Key Manager
(R/W)

## Register 27.8. DS_DATE_REG (0xOE20)

DS_DATE

DS_DATE Version control register (R/W)
```