

```markdown
Register 8.41. GPIO_EXT_INT_CLR_REG (0x01DC)

(reserved)                                                                 GPIO_EXT_COMP_ALL_O_INT_CLR
                                                                 GPIO_EXT_COMP_POS_O_INT_CLR
                                                                 GPIO_EXT_COMP_NEG_O_INT_CLR

31   2   1   0
+-----+------+------+------+
|    |    |    |Reset|
+-----+------+------+------+

GPIO_EXT_COMP_NEG_O_INT_CLR Write 1 to clear GPIO_EXT_COMP_NEG_O_INT.
(R/W)

GPIO_EXT_COMP_POS_O_INT_CLR Write 1 to clear GPIO_EXT_COMP_POS_O_INT.
(R/W)

GPIO_EXT_COMP_ALL_O_INT_CLR Write 1 to clear GPIO_EXT_COMP_ALL_O_INT.
(R/W)


Register 8.42. GPIO_EXT_VERSION_REG (0x01FC)

(reserved)                                                                 GPIO_EXT_DATE
31   28   27    0
+-----+------+------+------+
|    |    |    |Reset|
+-----+------+------+------+

GPIO_EXT_DATE Version control register. (R/W)


8.19.4 LP GPIO Matrix Registers

The addresses in this section are relative to LP GPIO matrix base address provided in Table 6.3-2 in Chapter 6
System and Memory.

For how to program reserved fields, please refer to Section VII .
```