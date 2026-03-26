

# 36.9 Registers

## 36.9.1 ISP Registers

The addresses in this section are relative to ISP base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 36.1. ISP_VER_DATE_REG (0x0000)

```
+---------------------------------------------------------------+
|                   ISP_VER_DATA                                |
|                                                               |
|  31  0x20210608                                               | Reset
+---------------------------------------------------------------+

ISP_VER_DATA  ISP version control register. (R/W)
```