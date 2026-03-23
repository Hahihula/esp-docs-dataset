

```markdown
## 2.8 Registers

The addresses in this section are relative to GDMA base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 2.1: GDMA_INT_RAW_CHn_REG (n: 0-2) (0x000+16*n)

| Bit | 31 | 30 | 29 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|-----|---|---|---|---|---|---|---|---|---|
|     |    |    |    |      |   |   |   |   |   |   |   | Reset | |

- GDMA_IN_DONE_CHn_INT_RAW: The raw interrupt bit turns to high level when the last data pointed by one receive descriptor has been received for RX channel O. (R/WTC/SS)
- GDMA_IN_SUC_EOF_CHn_INT_RAW: The raw interrupt bit turns to high level for RX channel O when the last data pointed by one receive descriptor has been received and the suc_eof bit in this descriptor is 1. For UHCIO, the raw interrupt bit turns to high level when the last data pointed by one receive descriptor has been received and no data error is detected for RX channel O. (R/WTC/SS)
- GDMA_IN_ERR_EOF_CHn_INT_RAW: The raw interrupt bit turns to high level when data error is detected only in the case that the peripheral is UHCIO for RX channel O. For other peripherals, this raw interrupt is reserved. (R/WTC/SS)
- GDMA_OUT_DONE_CHn_INT_RAW: The raw interrupt bit turns to high level when the last data pointed by one transmit descriptor has been transmitted to peripherals for TX channel O. (R/WTC/SS)
- GDMA_OUT_EOF_CHn_INT_RAW: The raw interrupt bit turns to high level when the last data pointed by one transmit descriptor has been read from memory for TX channel O. (R/WTC/SS)
- GDMA_IN_DSCR_ERR_CHn_INT_RAW: The raw interrupt bit turns to high level when detecting receive descriptor error, including owner error, the second and third word error of receive descriptor for RX channel O. (R/WTC/SS)
- GDMA_OUT_DSCR_ERR_CHn_INT_RAW: The raw interrupt bit turns to high level when detecting transmit descriptor error, including owner error, the second and third word error of transmit descriptor for TX channel O. (R/WTC/SS)

Continued on the next page...
```