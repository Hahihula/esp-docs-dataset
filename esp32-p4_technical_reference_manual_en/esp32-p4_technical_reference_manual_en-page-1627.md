

```markdown
Register 35.16. JPEG_INT_ENA_REG (0x003C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_DONE_INT_ENA | JPEG_DECCUNDET_INT_ENA | JPEG_TIMEOUT_INT_ENA | JPEG_MARKER_ERR_INT_ENA | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOF_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOF_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOF_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOF_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA | JPEG_EOF_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA | JPEG_EOR_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA | JPEG_OFS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA | JPEG_UNMATCH_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | JPEG_SIZERS_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |