

```markdown
| 31                                                                                                                                                                                                 | 3   2   1   0 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------|
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset          |

HP_SYSTEM_L2_MEM_ECC_ERR_INT_RAW The raw interrupt status of L2_MEM_ECC_ERR_INT, triggered when a one-bit flip error is detected and corrected by ECC. (R/WTC/SS)

HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_RAW The raw interrupt status of L2_MEM_EXCEED_ADDR_INT, triggered when access address exceeds limits in different modes.
Bypass mode: 0xff9fff
L2 cache 128 KB mode: 0xff80000
L2 cache 256 KB mode: 0xff60000
(R/WTC/SS)

HP_SYSTEM_L2_MEM_ERR_RESP_INT_RAW The raw interrupt status of L2_MEM_ERR_RESP_INT, triggered when an error response occurs. (R/WTC/SS)
```