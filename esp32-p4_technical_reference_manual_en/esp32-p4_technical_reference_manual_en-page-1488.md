

```markdown
Register 28.7. RSA_CONSTANT_TIME_REG (0x0820)

31 | [reserved] | RSA_CONSTANT_TIME
----------------------------------------------------------------------------------------------------
0   |            | 1 Reset

RSA_CONSTANT_TIME Configures the constant_time option.
O: Acceleration
1: No acceleration (default)
(R/W)


Register 28.8. RSA_SEARCH_ENABLE_REG (0x0824)

31 | [reserved] | RSA_SEARCH_ENABLE
----------------------------------------------------------------------------------------------------
0   |            | 0 Reset

RSA_SEARCH_ENABLE Configures the search option.
O: No acceleration (default)
1: Acceleration
This option should be used together with RSA_SEARCH_POS_REG. (R/W)


Register 28.9. RSA_SEARCH_POS_REG (0x0828)

31 | [reserved] | RSA_SEARCH_POS
----------------------------------------------------------------------------------------------------
0   |            | o Reset

RSA_SEARCH_POS Configures the starting address to start search. This field should be used together with RSA_SEARCH_ENABLE_REG. The field is only valid when RSA_SEARCH_ENABLE is high. (R/W)
```